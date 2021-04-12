---
title: Neutralino.storage
---

Neutralinojs has an in-built shared key-value storage. It's like a
global [`LocalStorage`](https://developer.mozilla.org/en-US/docs/Web/API/Window/localStorage) for all Neutralinojs modes.
Neutralinos.storage exposes methods for interacting with this storage feature.

## storage.putData(StorageWriterOptions)
Writes data into Neutralinojs shared storage. 

### StorageWriterOptions

- `bucket`: A key to indentify data.
- `data`: Data as a string.

```
await Neutralino.storage.putData({
  bucket: 'userDetails',
  data: {
    username: 'TestValue'
  }
});
```

## storage.getData(StorageReaderOptions)
Reads and returns data for a given Neutralinojs shared storage key. 

### StorageReaderOptions
- `bucket`: The key of the storage data record.

### Return object (awaited):
- `data`: Data string of the storage record.

```
let response = await Neutralino.storage.getData({
  bucket: 'userDetails'
});
console.log(`Data: ${response.data}`);
```