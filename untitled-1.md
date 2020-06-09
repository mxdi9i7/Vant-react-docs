# Rate

### [Demo](https://vant.bctc.io/?path=/story/rate--basic-usage)

#### Install

```text
import React from 'react';
import { Rate } from 'vant-react';
```

## Usage

**Basic Usage**

```text
<Rate currentRate={4} />
```

**Custom Icon**

```text
<Rate currentRate={4} icon='like' voidIcon='like-o' />
```

**Custom Color**

```text
<Rate currentRate={4} icon='like' voidIcon='like-o' color='#1989fa' />
```

#### Custom Count

```text
<Rate
      count={10}
      currentRate={4}
      icon='like'
      voidIcon='like-o'
      color='#1989fa'
/>
```

**Disabled**

```text
<Rate
      disabled
      currentRate={4}
      icon='like'
      voidIcon='like-o'
      color='#1989fa'
/>
```

**Read Only**

```text
<Rate
      readonly
      currentRate={4}
      icon='like'
      voidIcon='like-o'
      color='#1989fa'
/>
```

**Custom Gutter**

```text
<Rate
      gutter='8px'
      currentRate={4}
      icon='like'
      voidIcon='like-o'
      color='#1989fa'
/>
```

**Listen On Change**

```text
const [currentRate, setRate] = useState(4);

<h1>{currentRate}</h1>
      
<Rate
        change={(rate) => setRate(rate)}
        currentRate={currentRate}
        icon='like'
        voidIcon='like-o'
        color='#1989fa'
/>
```

## API

**Props**

| Attribute | Description | Type | Default | Required |
| :--- | :--- | :--- | :--- | :--- |
| `currentRate` | Current rate | _**number**_ | - | _optional_ |
| `text` | Count | _**number**_ | - | _optional_ |
| `size` | Icon size | _**string**_ | - | _optional_ |
| `icon` | Selected icon | _**string**_ | - | _optional_ |
| `gutter` | Icon gutter | _**string**_ | - | _optional_ |
| `voidIcon` | Void icon | _**string**_ | - | _optional_ |
| `*allowHalf` | Whether to allow half star | _**boolean**_ | `false` | _optional_ |
| `readonly` | Whether to be readonly | _**boolean**_ | `false` | _optional_ |
| `*touchable` | Whether to allow select rate by touch gesture | _**boolean**_ | `true` | _optional_ |
| `disabled` | Whether to disable rate | _**boolean**_ | `false` | _optional_ |
| `color` | Selected color | _**string**_ | - | _optional_ |
| `voidColor` | Void color | _**string**_ | - | _optional_ |
| `disabledColor` | Disabled color | _**string**_ | - | _optional_ |

**Event**

| Event | Description | Parameters |
| :--- | :--- | :--- |
| `change` | Triggered when rate changed | _current rate_ |

