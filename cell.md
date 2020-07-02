# index

### [Demo](https://vant.bctc.io/?path=/story/cell--basic-usage)

#### Install

```text
import React from 'react';
import { Popup } from 'vant-react';
```

## Usage

{% hint style="info" %}
Every popup should have its own state.
{% endhint %}

```text
const [centerPopup, setCenterPopup] = useState(false);

<Button click={() => {setCenterPopup(true)}}/>
<Popup isActive={centerPopup} setActive={setCenterPopup} />
```

#### Type

```text
<Popup type='top'/>
<Popup type='bottom'/>
<Popup type='left'/>
<Popup type='right'/>
```

#### Size

```text
<Popup size={['200px', '200px']} />
<Popup size={['50vw', '60vh']} />
```

#### Content

```text
<Popup text={{
          text: 'It`s a popup',
          color: '#666',
          fontSize: '30px',
          textAlign: 'center'
        }} />
<Popup content={<Component />} />
```

#### CloseIcon

```text
<Popup closeable />
<Popup closeable closeIcon={{ name: 'close', size: '20px' }} />
<Popup closeable closeIconPosition={{ top: '40px', left: '40px' }} />
```

#### Round Corner

```text
<Popup borderRadius='50px' />
```

#### Custom Color

```text
<Popup color='#b90000' />
<Popup color='rgba(234, 123, 232,0.4)' />
```

#### Action

```text
<Popup text={{
          text: 'Click me',
          color: '#000',
          fontSize: '30px',
          textAlign: 'center'
        }}
       size={['300px', '60px']}
       click={(e) => { alert(e) }} />
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

#### Event

<table>
  <thead>
    <tr>
      <th style="text-align:left">Event</th>
      <th style="text-align:left">Description</th>
      <th style="text-align:left">Arguments</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>click</code>
      </td>
      <td style="text-align:left">
        <p>Triggered when click text in popup</p>
        <p>and not disabled or loading</p>
      </td>
      <td style="text-align:left"><em>event: Event</em>
      </td>
    </tr>
  </tbody>
</table>

