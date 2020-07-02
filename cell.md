# Cell

### [Demo](https://vant.bctc.io/?path=/story/cell--basic-usage)

#### Install

```text
import React from 'react';
import { Cell } from 'vant-react';
```

## Usage

#### Basic Usage

```text
<Cell
      title={{ text: 'Title', fontSize: '14px' }}
      content={{ text: 'Content', fontSize: '12px' }}
    />
<Cell
      title={{ text: 'Title', fontSize: '14px' }}
      content={{ text: 'Content', fontSize: '12px' }}
      description={{ text: 'description', fontSize: '12px' }}
    />
```

#### Cell Icon

```text
<Cell titleIcon={{ name: 'location-o', size: '12px' }}
      title={{ text: 'Title', fontSize: '14px' }}
      contentIcon={{ name: 'arrow', size: '12px' }}
      content={{ text: 'Content', fontSize: '12px' }} 
    />
```

#### Cell Tag

```text
<Cell
      title={{ text: 'Title', fontSize: '14px' }}
      Tag={<Tag type='danger' text='Tag' />}
      content={{ text: 'Content', fontSize: '12px' }}
    />
```

#### Round Cell

```text
<Cell title={{ text: 'Title', fontSize: '14px' }} round />
```

#### Value Only

```text
<Cell title={{ text: 'Title', fontSize: '14px' }} round />
```

#### URL

```text
<Cell
      title={{ text: 'URL', fontSize: '14px' }}
      url='www.google.com'
      replace
    />
```

#### Action

```text
<Cell
      title={{ text: 'Click', fontSize: '14px' }}
      click={(e) => {
        alert(e);
      }}
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
      <td style="text-align:left"><code>title</code>
      </td>
      <td style="text-align:left">Cell title</td>
      <td style="text-align:left"><em><b>object</b></em>
      </td>
      <td style="text-align:left">-</td>
      <td style="text-align:left"><em>optional</em>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>titleIcon</code>
      </td>
      <td style="text-align:left">Left side icon name</td>
      <td style="text-align:left"><em><b>object</b></em>
      </td>
      <td style="text-align:left"><em><b>-</b></em>
      </td>
      <td style="text-align:left"><em>optional</em>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>content</code>
      </td>
      <td style="text-align:left">Cell content</td>
      <td style="text-align:left"><em><b>object</b></em>
      </td>
      <td style="text-align:left">-</td>
      <td style="text-align:left"><em>optional</em>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>contentIcon</code>
      </td>
      <td style="text-align:left">Right side icon name</td>
      <td style="text-align:left"><em><b>object</b></em>
      </td>
      <td style="text-align:left">-</td>
      <td style="text-align:left"><em>optional</em>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>description</code>
      </td>
      <td style="text-align:left">Cell description</td>
      <td style="text-align:left"><em><b>object</b></em>
      </td>
      <td style="text-align:left">-</td>
      <td style="text-align:left"><em>optional</em>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>Tag</code>
      </td>
      <td style="text-align:left">Cell tag</td>
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
      <td style="text-align:left"><code>url</code>
      </td>
      <td style="text-align:left">Link URL</td>
      <td style="text-align:left"><em><b>string</b></em>
      </td>
      <td style="text-align:left">-</td>
      <td style="text-align:left"><em>optional</em>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>replace</code>
      </td>
      <td style="text-align:left">Whether open in current tab</td>
      <td style="text-align:left"><em><b>boolean</b></em>
      </td>
      <td style="text-align:left">-</td>
      <td style="text-align:left"><em>optional</em>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>round</code>
      </td>
      <td style="text-align:left">Whether to be round button</td>
      <td style="text-align:left"><em><b>boolean</b></em>
      </td>
      <td style="text-align:left">-</td>
      <td style="text-align:left"><em>optional</em>
      </td>
    </tr>
  </tbody>
</table>

#### Event

| Event | Description | Arguments |
| :--- | :--- | :--- |
| `click` | Triggered when click cell and not disabled or loading | _event: Event_ |

