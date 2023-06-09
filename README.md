# vite-require-main

Like Webpack's require

such as：
```
<img :src="require(`assets/img/home/svg/icon-usr${iconName}.svg`)" alt />
```

📦 Out of the box  


## Install

```bash
npm i vite-require-main -D
```

## Usage

```js
import { viteRequire } from 'vite-require-main'
export default {
  plugins: [
    viteRequire(/* options */)
  ]
}
```

## API

viteRequire([options])

```ts
export interface Options {
  extensions?: string[]
  filter?: (id: string) => false | void
  dynamic?: {
    /**
     * 1. `true` - Match all possibilities as much as possible, More like `webpack`
     * 2. `false` - It behaves more like `@rollup/plugin-dynamic-import-vars`
     * @default true
     */
    loose?: boolean
  }
}
```

## Credits

Thanks to: [vite-require](https://github.com/vite-plugin/vite-require)
