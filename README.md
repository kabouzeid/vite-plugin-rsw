# vite-plugin-rsw

> wasm-pack plugin for vite@v2

## TODO

- [x] watch crates
- [x] multiple crates
- [ ] vite build

## Getting Started

> Install rsw

```bash
npm i -D vite-plugin-rsw
```

> vite.config.ts

```js
import { defineConfig } from 'vite'
import { ViteRsw } from 'vite-plugin-rsw';
import path from 'path';

export default defineConfig({
  plugins: [
    ViteRsw({
      // target: 'web',
      mode: 'release',
      crates: [
        {
          path: 'rsw',
          outName: 'hey', // out filename
          scope: 'l8n', // package organization
        },
        {
          path: path.resolve(__dirname, 'rsw-test')
          // outName: '',
          // scope: '',
        },
      ],
    }),
  ],
})
```
