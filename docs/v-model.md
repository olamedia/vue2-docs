# Text and Textarea elements

> text and textarea elements use **value** property and **input** event

## Text
```vue
<input type="text" v-model="value" />
<input type="text" :value="value" @input="emit('input', $event.target.value)" />
<input type="text" :value="value" @input="onInput($event.target.value)" />
```

## Textarea
> Interpolation on textareas (<textarea>{{text}}</textarea>) won't work
```vue
<textarea v-model="message"></textarea>
<textarea :value="value" @input="emit('input', $event.target.value)"></textarea>
<textarea :value="value" @input="onInput($event.target.value)"></textarea>
```

# Checkboxes and radiobuttons

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

# Select fields

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
  <option v-for="option in options" :value="option.value">
    {{ option.text }}
  </option>
</select>
```

## Vue2 Custom components
```vue
<CustomInput
  :value="value"
  @input="newValue => value = newValue"
/>
```
## Vue3 Custom components
```vue
<CustomInput
  :modelValue="value"
  @update:modelValue="newValue => value = newValue"
/>
```
