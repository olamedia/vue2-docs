

> checkboxes and radiobuttons use **checked** property and **change** event

## Checkbox
```vue
<input type="checkbox" :value="formValue" :checked="value" @change="emit('input', $event.target.checked)" />
<input type="checkbox" :value="formValue" :checked="value" @change="onChange($event.target.checked)" />
```

## Radio
```vue
<input type="radio" :value="formValue" :checked="value" @change="emit('input', $event.target.checked)" />
<input type="radio" :value="formValue" :checked="value" @change="onChange($event.target.checked)" />
```
