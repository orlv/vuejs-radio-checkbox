# vuejs-radio-checkbox

Checkbox set with radio button behavior

#### Installation

```
npm i -D vuejs-radio-checkbox
```


#### Example

```
<radio-checkbox class="radio-checkbox" :inputs="inputs" v-model="value"/>
```
```
import RadioCheckbox from 'vuejs-radio-checkbox'
```
```
components: {
  RadioCheckbox
}

data () {
  return {
    value: '',
    inputs: [
      {value: '1', label: 'Val 1', title: 'Value 1'},
      {value: '2', label: 'Val 2', title: 'Value 2'},
      {value: '3', label: 'Val 3', title: 'Value 3'},
      {value: '4', label: `Val 4'`, title: 'Value 4'},
      {value: '5', label: `Val 5'`, title: 'Value 5'},
      {value: '6', label: `Val 6'`, title: 'Value 6'}
    ]
  }
}
```
