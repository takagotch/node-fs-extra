### node-fs-extra
---
https://github.com/jprichardson/node-fs-extra

```js
// lib/__tests__/promise.test.js\
'use strict'

const assert = require('assert')
const fs = require('fs')
const fse = require('..')

const method = [
  'copy',
  'emptyDir',
  'ensureFile',
  'ensureDir',
  'mkdirs',
  'move',
  'readJson',
  'readJSON',
  'remove',
]

describe('promise support', () => {
  methods.forEach(method => {
    it(method, done => {
      fse[method]().catch(() => done())
    })
  })
  
  if (Object.getOwnPropertyDescriptor(fs, 'promises')) {
    it('provides fse.promises API', () => {
      const desc = Object.getOwnPropertyDescriptor(fse, 'promises')
      assert.ok(desc)
      assert.strictEqual(typeof desc.get, 'function')
    })
  }
})
```

```
```

```
```
