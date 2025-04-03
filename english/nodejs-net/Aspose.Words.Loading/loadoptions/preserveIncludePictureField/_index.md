---
title: LoadOptions.preserveIncludePictureField property
linktitle: preserveIncludePictureField property
articleTitle: preserveIncludePictureField property
second_title: Aspose.Words for NodeJs
description: "LoadOptions.preserveIncludePictureField property. Gets or sets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats"
type: docs
weight: 120
url: /nodejs-net/Aspose.Words.Loading/loadoptions/preserveIncludePictureField/
---

## LoadOptions.preserveIncludePictureField property

Gets or sets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats.
The default value is ``false``.



```js
get preserveIncludePictureField(): boolean
```

### Remarks

By default, the INCLUDEPICTURE field is converted into a shape object. You can override that if you need
the field to be preserved, for example, if you wish to update it programmatically. Note however that this
approach is not common for Aspose.Words. Use it on your own risk.

One of the possible use cases may be using a MERGEFIELD as a child field to dynamically change the source path
of the picture. In this case you need the INCLUDEPICTURE to be preserved in the model.




### See Also

* module [Aspose.Words.Loading](../../)
* class [LoadOptions](../)

