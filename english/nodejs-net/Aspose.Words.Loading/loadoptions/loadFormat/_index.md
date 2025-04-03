---
title: LoadOptions.loadFormat property
linktitle: loadFormat property
articleTitle: loadFormat property
second_title: Aspose.Words for NodeJs
description: "LoadOptions.loadFormat property. Specifies the format of the document to be loaded"
type: docs
weight: 90
url: /nodejs-net/aspose.words.loading/loadoptions/loadFormat/
---

## LoadOptions.loadFormat property

Specifies the format of the document to be loaded.
Default is [LoadFormat.Auto](../../../aspose.words/loadformat/#Auto).



```js
get loadFormat(): Aspose.Words.LoadFormat
```

### Remarks

It is recommended that you specify the [LoadFormat.Auto](../../../aspose.words/loadformat/#Auto) value and let Aspose.Words detect
the file format automatically. If you know the format of the document you are about to load, you can specify the format
explicitly and this will slightly reduce the loading time by the overhead associated with auto detecting the format.
If you specify an explicit load format and it will turn out to be wrong, the auto detection will be invoked and a second
attempt to load the file will be made.




### See Also

* module [Aspose.Words.Loading](../../)
* class [LoadOptions](../)

