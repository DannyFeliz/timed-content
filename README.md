# vue-timed-content

> Shows or hides a content based on a given time range

[<img src="https://img.shields.io/npm/dt/vue-timed-content.svg">](https://www.npmjs.com/package/vue-timed-content)
[<img src="https://img.shields.io/npm/v/vue-timed-content.svg">](https://www.npmjs.com/package/vue-timed-content)

## Demo

[![Edit Vue Timed Content Demo](https://codesandbox.io/static/img/play-codesandbox.svg)](https://codesandbox.io/s/vue-timed-content-demo-k3b5c?fontsize=14&hidenavigation=1&module=%2Fsrc%2FApp.vue&theme=dark)

## Props

<table>
  <thead>
    <tr>
      <th>Prop</th>
      <th>Description</th>
      <th>Type</th>
      <th>Required</th>
      <th>Default</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>from</td>
      <td>Initial date</td>
      <td>Date</td>
      <td>true</td>
      <td></td>
    </tr>
    <tr>
      <td>to</td>
      <td>End date</td>
      <td>Date</td>
      <td>true</td>
      <td></td>
    </tr>
    <tr>
      <td>time-zone</td>
      <td>Timezone used to calculate if the dates are in range</td>
      <td>String</td>
      <td>false</td>
      <td>Your local timezone</td>
    </tr>
  </tbody>
</table>

## Events

<table>
  <thead>
    <tr>
      <th>Event</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>show</td>
      <td>When content goes from being hidden to visible</td>
    </tr>
    <tr>
      <td>hide</td>
      <td>When content goes from being visible to hidden</td>
    </tr>

  </tbody>
</table>

## Usage

```vue
<template>
  <div>
    <p>If you don't see anything it's because you are not in the range to be able view the content</p>
    <timed-content
      :from="new Date('2020/04/01 00:00:00')"
      :to="new Date('2020/04/01 23:59:59')"
      time-zone="America/Santo_Domingo"
    >
      <p>Some April Fools' Day joke 🃏</p>
    </timed-content>
  </div>
</template>

<script>
import TimedContent from "vue-timed-content";

export default {
  components: {
    TimedContent
  }
};
</script>
```

## Project setup

```
npm install
```

### Compiles and hot-reloads for development

```
npm run serve
```

### Compiles and minifies for production

```
npm run build
```

### Lints and fixes files

```
npm run lint
```

### Customize configuration

See [Configuration Reference](https://cli.vuejs.org/config/).
