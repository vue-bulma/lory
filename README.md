# lory

☀ Touch enabled minimalistic slider for Vue, it is based on [lory](https://github.com/meandmax/lory).


## Installation

```console
$ npm install vue-lory --save
```


## Examples

```vue
<template>
  <lory :options="{ enableMouseEvents: true, infinite: 1 }">
    <item>1</item>
    <item>2</item>
    <item>3</item>
    <item>4</item>
    <item>5</item>
    <item>6</item>
    <prev slot="actions"></prev>
    <next slot="actions"></next>
  </lory>
</template>

<script>
import { Lory, Item, Prev, Next } from 'vue-lory'

export default {
  components: {
    Lory,
    Item,
    Prev,
    Next
  }
}
</script>
```


## Badges

![](https://img.shields.io/badge/license-MIT-blue.svg)
![](https://img.shields.io/badge/status-stable-green.svg)

---

> [fundon.me](https://fundon.me) &nbsp;&middot;&nbsp;
> GitHub [@fundon](https://github.com/fundon) &nbsp;&middot;&nbsp;
> Twitter [@_fundon](https://twitter.com/_fundon)

