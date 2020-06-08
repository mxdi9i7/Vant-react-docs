# Field

### [Demo](https://vant.bctc.io/?path=/story/field--basic-usage)

#### Install

```text
import React from 'react';
import { Field } from 'vant-react';
```

## Usage

#### Basic Usage

```text
<Field />
```

#### Require Field

```text
<Field label='Required' required />
```

#### Custom Types

```text
<Field label='Text' type='text' />
<Field label='Phone' type='tel' />
<Field label='Digit' type='digit' />
<Field label='Number' type='number' />
<Field label='Password' type='password' />
```

#### Disabled

```text
<Field disabled value='Input Disabled' />
<Field readonly value='Input Readonly' />
```

#### Colon

```text
<Field label='Colon' colon />
```

#### ShowIcon

```text
<Field label='Left Icon' leftIcon='music-o' />
<Field label='Right Icon' rightIcon='success' />
<Field labelWidth='150px' label='Label Icon' labelIcon='search' />
```

#### Field Events

```text
const [value, setValue] = useState('');
const [isFocus, setFocus] = useState(false);

<p>Value: {value}</p>

<Field
        leftIcon='smile-o'
        placeholder='Show clear icon'
        rightIcon='success'
        value={value}
        input={(e) => setValue(e.target.value)}
        clear={() => setValue('')}
        clearable
/>
<Field 
        leftIcon='smile-o' 
        placeholder='Click event' 
        rightIcon='success' 
/>
<Field
        leftIcon='smile-o'
        placeholder='Input focus state'
        rightIcon={isFocus ? 'success' : 'cross'}
        focus={() => setFocus(true)}
        blur={() => setFocus(false)}
/>
<Field
        leftIcon='smile-o'
        placeholder='Input click event'
        clickable
        clickInput={() => alert('Input clicked')}
/>
<Field
        leftIcon='smile-o'
        rightIcon='fire-o'
        placeholder='Input left and right icon click'
        clickable
        clickLeftIcon={() => alert('Left Icon Clicked')}
        clickRightIcon={() => alert('Right Icon Clicked')}
/>
```

#### Field Ref

```text
const [containerRef, setContainerRef] = useState(null);
const [fieldRef, setFieldRef] = useState(null);
const [clickOutside, setClickOutside] = useState(false);

window.addEventListener('click', (e) => {
    if (
      containerRef !== undefined &&
      containerRef.current &&
      !containerRef.current.contains(e.target)
    ) {
      setClickOutside(true);
    } else {
      setClickOutside(false);
    }
  });


<p>
    Container Ref element name:
    {
      containerRef && containerRef.current.localName
    }
</p>
<p>
    Field Ref element name:{' '}
    {
      fieldRef && fieldRef.current.localName
    }
</p>

<Field
        placeholder={`Click outside? ${clickOutside}`}
        leftIcon='music-o'
        rightIcon='success'
        getContainerRef={(ref) => setContainerRef(ref)}
        getFieldRef={(ref) => setFieldRef(ref)}
/>
```

#### Auto Focus

```text
<Field label='Error input' error errorMessage='Invalid input info' />
```

#### Error Info

```text
<Field label='Error input' error errorMessage='Invalid input info' />
```

#### Max Length Word Limit

```text
const [value, setValue] = useState('');

<Field
        value={value}
        input={(e) => setValue(e.target.value)}
        label='Max length'
        maxLength={5}
        showWordLimit
/>
```

#### Field With Button

```text
<Field
        label='SMS'
        placeholder='SMS'
        button=
        {
          <Button
            size='small'
            click={() => alert('Message sent!')}
            text='Send SMS'
            type='primary'
          />
        }
/>
```

#### Formatter

```text
const [value, setValue] = useState('');

<Field
        label='Text Only'
        placeholder='No Numbers'
        value={value}
        input={(e) => setValue(e.target.value)}
        formatter={(value) => pattern.test(value)}
/>
```

#### Label Utilities

```text
<Field label='Long 220px label' labelClass='pant' labelWidth='220px' />
```

#### Label Input Alignment

```text
<Field
      label='Label Center'
      placeholder='Input Right'
      labelWidth='190px'
      labelAlign='center'
      inputAlign='right'
/>
<Field
      label='Label Right'
      placeholder='Input Center'
      labelWidth='190px'
      inputAlign='center'
      labelAlign='right'
/>
<Field
      label='Error Center'
      placeholder='Input Center'
      labelWidth='190px'
      inputAlign='center'
      labelAlign='right'
      error
      errorMessage='Something went wrong'
      errorAlign='center'
/>
<Field
      label='Error Right'
      placeholder='Input Center'
      labelWidth='190px'
      inputAlign='center'
      labelAlign='right'
      errorMessage='Something went wrong'
      errorAlign='right'
      error
/>
```

#### Auto Resize

```text
<Field />
```

## API

#### Props

| Attribute | Description | Type | Default | Required |
| :--- | :--- | :--- | :--- | :--- |
| `value` | Filed value | _**string**_ | - | _optional_ |
| `type` | Can be set to `text` `tel` `digit` `number` `password`  | _**string**_ | `text` | _optional_ |
| `label` | Field label | _**string**_ | - | _optional_ |
| `name` | Name | _**string**_ | - | _optional_ |
| `placeholder` | Placeholder | _**string**_ | - | _optional_ |
| `readonly` | Whether to be readonly | _**boolean**_ | `false` | _optional_ |
| `disabled` | Whether to display colon after label | _**boolean**_ | `false` | _optional_ |
| `colon` | Whether to be readonly | _**boolean**_ | `false` | _optional_ |
| `labelIcon` | Label icon that appears on the left | _**string**_ | - | _optional_ |
| `leftIcon` | Left side icon name | _**string**_ | - | _optional_ |
| `rightIcon` | Right side icon name | _**string**_ | - | _optional_ |
| `clearable` | Whether to be clearable | _**boolean**_ | `false` | _optional_ |
| `clickable` | Whether to show click feedback when clicked | _**boolean**_ | `false` | _optional_ |
| `autofocus` | Whether to auto focus | _**boolean**_ | `false` | _optional_ |
| `error` | Whether to show error info | _**boolean**_ | `false` | _optional_ |
| `error-message` | Error message | _**string**_ | - | _optional_ |
| `maxLength` | Max length of value | _**number**_ | - | _optional_ |
| `showWordLimit` | Whether to show word limit, need to set `maxLength` prop | _**boolean**_ | `false` | _optional_ |
| `formatter` | Input value formatter | _**Function**_ | `true` | _optional_ |
| `labelClass` | Label className | _**string**_ | - | _optional_ |
| `labelWidth` | Label width | _**string**_ | - | _optional_ |
| `labelAlign` | Label align, can be set to`center` `right`  | _**TAlignment**_ | `left` | _optional_ |
| `inputAlign` | Input align, can be set to`center` `right`  | _**TAlignment**_ | `left` | _optional_ |
| `errorAlign` | Error message align, can be set to`center` `right`  | _**TAlignment**_ | `left` | _optional_ |
| `required` | Whether to show required mark | _**boolean**_ | `false` | _optional_ |
| `border` | Whether to show inner border | _**boolean**_ | `true` | _optional_ |

#### Event

| Event | Description | Arguments |
| :--- | :--- | :--- |
| `input` | Triggered when input value changed | _value: String_ |
| `clear` | Triggered when click clear icon | _event: Event_ |
| `click` | Triggered when click Field | _event: Event_ |
| `clickInput` | Triggered when click input | _event: Event_ |
| `focus` | Triggered when input gets focus | _event: Event_ |
| `blur` | Triggered when input loses focus | _event: Event_ |
| `clickLeftIcon` | Triggered when click the left icon of Field | _event: Event_ |
| `clickRightIcon` | Triggered when click the right icon of Field | _event: Event_ |
| `getContainerRef` | Triggered when container ref is not undefined nor null | _event: Event_ |
| `getFieldRef` | Triggered when Field ref is not undefined nor null | _event: Event_ |
| `focus` | Triggered when input gets focus | _event: Event_ |

