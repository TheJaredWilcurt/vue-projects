# vue-projects

Vue Projects made by TheJaredWilcurt.

The idea of this repo is that you will install it like so:


```json
{
  "dependencies": {
    "vue-projects": "github:TheJaredWilcurt/vue-projects"
  }
}
```

and then

```js
import VueProjects from 'vue-projects/VpCards.vue';
```

```html
<VueProjects :includeId="true" />
```

or you can do

```html
<iframe src="https://thejaredwilcurt.com/vue-projects/#/?style=background:#000;color:#FFF;" />
```

but then you have to deal with layout stuff on different screen sizes.
