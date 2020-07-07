# Slider

### [Demo](http://localhost:9009/?path=/story/popup--default-popup)

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

<table>
  <thead>
    <tr>
      <th style="text-align:left">Attribute</th>
      <th style="text-align:left">Description</th>
      <th style="text-align:left">Type</th>
      <th style="text-align:left">Default</th>
      <th style="text-align:left">Required</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>type</code>
      </td>
      <td style="text-align:left">Can be set to <code>left</code>  <code>right</code>  <code>top</code>  <code>bottom</code>
      </td>
      <td style="text-align:left"><em><b>string</b></em>
      </td>
      <td style="text-align:left"><code>center</code>
      </td>
      <td style="text-align:left"><em>optional</em>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>text</code>
      </td>
      <td style="text-align:left">
        <p>Text to be displayed in popup ,<code>{text,color,size,</code>
        </p>
        <p><code>textAlign}</code>
        </p>
      </td>
      <td style="text-align:left"><em><b>object</b></em>
      </td>
      <td style="text-align:left">-</td>
      <td style="text-align:left"><em>optional</em>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>color</code>
      </td>
      <td style="text-align:left">Popup background-color, in hex value:<code>#b90000</code>, in gradient
        value in rgba:<code>rgb(210,210,210,0.4)</code>
      </td>
      <td style="text-align:left"><em><b>string</b></em>
      </td>
      <td style="text-align:left">-</td>
      <td style="text-align:left"><em>optional</em>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>borderRadius</code>
      </td>
      <td style="text-align:left">round corner</td>
      <td style="text-align:left"><em><b>string</b></em>
      </td>
      <td style="text-align:left">-</td>
      <td style="text-align:left"><em>optional</em>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>size</code>
      </td>
      <td style="text-align:left">popup size ,<code>[width,height]</code>
      </td>
      <td style="text-align:left"><em><b>array</b></em>
      </td>
      <td style="text-align:left">-</td>
      <td style="text-align:left"><em>optional</em>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>padding</code>
      </td>
      <td style="text-align:left">
        <p>content padding ,</p>
        <p><code>10px</code>  <code>0 20px</code>
        </p>
      </td>
      <td style="text-align:left"><em><b>string</b></em>
      </td>
      <td style="text-align:left">-</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><code>content</code>
      </td>
      <td style="text-align:left">Component to be displayed in popup</td>
      <td style="text-align:left">
        <p><em><b>React</b></em>
        </p>
        <p><em><b>Element</b></em>
        </p>
      </td>
      <td style="text-align:left">-</td>
      <td style="text-align:left"><em>optional</em>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>closeable</code>
      </td>
      <td style="text-align:left">show close icon in popup</td>
      <td style="text-align:left"><em><b>boolean</b></em>
      </td>
      <td style="text-align:left"><code>false</code>
      </td>
      <td style="text-align:left"><em>optional</em>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>closeIcon</code>
      </td>
      <td style="text-align:left">custom your close icon ,<code>{iconName, iconSize}</code>
      </td>
      <td style="text-align:left"><em><b>object</b></em>
      </td>
      <td style="text-align:left">-</td>
      <td style="text-align:left"><em>optional</em>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>closeIconPosition</code>
      </td>
      <td style="text-align:left"><code>Ex: { top: &apos;40px&apos;, left: &apos;40px&apos; }</code>
      </td>
      <td style="text-align:left"><em><b>object</b></em>
      </td>
      <td style="text-align:left">-</td>
      <td style="text-align:left"><em>optional</em>
      </td>
    </tr>
  </tbody>
</table>

