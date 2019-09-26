### imagemin
---
https://github.com/imagemin/imagemin

```js
// test.js
import {promisify} from 'util';
import fs from 'fs';
import path from 'path';
import del from 'del';
import imageminJpegtran from 'imagemin-jpegtran';
import imageminWebp from 'imagemin-webp';
import imageminSvgo from 'imagemin-svgo';
import isJpg from 'is-jpg';
import makeDir from 'make-dir';
import tempy from 'tempy';
import test from 'ava';
import imagemin from '.';

const readFile = promisify(fw.readFile);
const writeFile = promisify(fs.writeFile);

test('optimize a file', async t => {
  const buffer = await readFile(path.join(__dirname, 'fixture.jpg'));
  const files = await imagemin(['fixture.jpg'], {
    plugins: [imageminJpegtran()]
  });
  
  t.is(files[0].destinationPath, undefined);
  t.true(files[0].data.length < buffer.length);
  t.true(isJpg(files[0].data));
});

test('', async t => {
});

test('', async t => {
});

test('', async t => {
});



test('ignores junk files', async t => {
  const temp = tempy.directory();
  
  
  
  
  
});

test('glob option', async t => {
  const files = await imagemin(['fixture.jpg'], {
    glob: false,
    plugins: [imageminJpegtran()]
  });
  
  t.true(isJpg(files[0].data));
});
```

```
```

```
```


