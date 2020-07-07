# Slider

### [Demo](https://vant.bctc.io/?path=/story/slider--basic-usage)

#### Install

```text
import React from 'react';
import { Slider } from 'vant-react';
```

## Usage

{% hint style="info" %}
Every slider should have its own state. And if we have more than one slider on the same page, each slider should have a unique id.
{% endhint %}

```text
const [value, setValue] = useState(0)
  
<Slider id='a' value={value} setValue={setValue} />
```

#### Slide Range

```text
<Slider range={{ min: '-50px', max: '50px' }} />
```

#### Slide Step

```text
<Slider step={10} />
```

#### Disabled

```text
<Slider disabled />
```

#### Show Value

```text
<Slider   sliderStyle={{
          color: '#000',
          fontSize: '12px',
          backgroundColor: '#fff',
          borderRadius: '5px',
          borderColor: '#000'
        }}
        sliderSize={{ width: '30px', height: '20px' }}
        hasValue
      />
```

#### Custom Size   

```text
<Slider   size={{ width: '300px', height: '10px' }}
          sliderSize={{ width: '30px', height: '30px' }}
        />
```

#### Custom Style

```text
<Slider   size={{ width: '400px', height: '10px' }}
          sliderStyle={{ backgroundColor: '#2F4F4F' }}
          inactiveColor='transparent'
          activeColor='#b90000'
        />
```

## API

#### Props

| Attribute | Description | Type | Default | Required |
| :--- | :--- | :--- | :--- | :--- |
| `hasValue` | Whether show value in slider button | _**boolean**_ | `false` | _optional_ |
| `disabled` | Whether ban the slider | _**boolean**_ | `false` | _optional_ |
| `activeColor` | Color in the fill bar | _**string**_ | - | _optional_ |
| `inactiveColor` | Color in the wrapper bar | _**string**_ | - | _optional_ |
| `size` | Slider size `{width:string,height:string}` | _**object**_ | - | _optional_ |
| `sliderSize` | Slider button size | _**object**_ | - | _optional_ |
| `sliderStyle` | Custom  slider button style from color, fontSize, backgroundColor, borderRadius and borderColor | _**object**_ | - | _optional_ |
| `range` | Slider range `{min:string,max:string}` | _**object**_ | - | _optional_ |
| `id` | If we have more than one slider on the same page, each slider should have a unique id. | _**string**_ | - | _optional_ |
| `step` | `Step length in each slide` | _**number**_ | - | _optional_ |
| `value` | Value state | _**number**_ | - | _required_ |
| `setValue` | setState | _**function**_ | - | _required_ |



