---
title: LoadOptions.ignoreOleData property
linktitle: ignoreOleData property
articleTitle: ignoreOleData property
second_title: Aspose.Words for NodeJs
description: "LoadOptions.ignoreOleData property. Specifies whether to ignore the OLE data."
type: docs
weight: 70
url: /nodejs-net/Aspose.Words.Loading/loadoptions/ignoreOleData/
---

## LoadOptions.ignoreOleData property

Specifies whether to ignore the OLE data.


```js
get ignoreOleData(): boolean
```

### Remarks

Ignoring OLE data may reduce memory consumption and increase performance without data lost in a case when destination format does not support OLE objects.

The default value is ``False``.




### Examples

Shows how to ingore OLE data while loading.

```js
// Ignoring OLE data may reduce memory consumption and increase performance
// without data lost in a case when destination format does not support OLE objects.
let loadOptions = new aw.Loading.LoadOptions();
loadOptions.ignoreOleData = true;
let doc = new aw.Document(base.myDir + "OLE objects.docx", loadOptions);

doc.save(base.artifactsDir + "LoadOptions.ignoreOleData.docx");
```

### See Also

* module [Aspose.Words.Loading](../../)
* class [LoadOptions](../)

