> text and textarea elements use **value** property and **input** event

## Text
```vue
<input type="text" v-model="value" />
<input type="text" :value="value" @input="emit('input', $event.target.value)" />
<input type="text" :value="value" @input="onInput($event.target.value)" />
```

## Textarea
> Interpolation on textareas **(<textarea>{{text}}</textarea>) won't work**. Use v-model instead.
```vue
<textarea v-model="message"></textarea>
<textarea :value="value" @input="emit('input', $event.target.value)"></textarea>
<textarea :value="value" @input="onInput($event.target.value)"></textarea>
```

> checkboxes and radiobuttons use **checked** property and **change** event

## Checkbox
```vue
<input type="checkbox" :value="formValue" v-model="value" />
<input type="checkbox" :value="formValue" :checked="value" @change="emit('input', $event.target.checked)" />
<input type="checkbox" :value="formValue" :checked="value" @change="onChange($event.target.checked)" />
```

## Radio
```vue
<input type="radio" :value="formValue" v-model="value" />
<input type="radio" :value="formValue" :checked="value" @change="emit('input', $event.target.checked)" />
<input type="radio" :value="formValue" :checked="value" @change="onChange($event.target.checked)" />
```

> select fields use **value** as a prop and **change** as an event

## Select
```vue
<select v-model="value">
  <option disabled value="">Please select one</option>
  <option>A</option>
  <option>B</option>
  <option>C</option>
</select>
<select v-model="value">
  <option v-for="option in options" v-bind:value="option.value">
    {{ option.text }}
  </option>
</select>
```
