<template>
    <div>
        <div v-for="checkbox in inputs">
            <input class="radio-checkbox" type="checkbox" :id="'radio-checkbox-' + _uid + '-' + checkbox.value"
                   :value="checkbox.value" v-model="inputsList" @click="click(checkbox.value)"/>
            <label class="radio-checkbox-label" :for="'radio-checkbox-' + _uid + '-' + checkbox.value"
                   :title="checkbox.title">{{ checkbox.label }}</label>
        </div>
    </div>
</template>

<script>
  export default {
    data: function () {
      return {
        inputsList: []
      }
    },

    props: ['inputs', 'value'],

    created () {
      if (this.value) {
        this.inputsList.push(this.value)
      }
    },

    watch: {
      value: function (value) {
        this.inputsList.length = 0
        this.inputsList.push(value)
      }
    },

    methods: {
      click: function (value) {
        if (value === this.value) {
          this.$emit('input', undefined)
        } else {
          this.$emit('input', value)
        }
      }
    }
  }
</script>
