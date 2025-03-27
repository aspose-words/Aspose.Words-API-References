---
title: ChmLoadOptions.originalFileName property
linktitle: originalFileName property
articleTitle: originalFileName property
second_title: Aspose.Words for NodeJs
description: "ChmLoadOptions.originalFileName property. The name of the CHM file"
type: docs
weight: 20
url: /nodejs-net/Aspose.Words.Loading/chmloadoptions/originalFileName/
---

## ChmLoadOptions.originalFileName property

The name of the CHM file.
Default value is ``None``.



```js
get originalFileName(): string
```

### Remarks

CHM documents may contain links that reference the same document by file name. Aspose.Words supports such links
and normally uses [Document.originalFileName](../../../Aspose.Words/document/originalFileName/) to check whether the file referenced by a link
is the file that is being loaded. If a document is loaded from a stream, its original file name should be specified
explicitly via this property, since it cannot be determined automatically.


If a CHM document is loaded from a file and a non-null value for this property is specified, the value will take
priority over the actual name of the file stored in [Document.originalFileName](../../../Aspose.Words/document/originalFileName/).





### Examples

Shows how to resolve URLs like "ms-its:myfile.chm::/index.htm".

```js
// Our document contains URLs like "ms-its:amhelp.chm::....htm", but it has a different name,
// so file links don't work after saving it to HTML.
// We need to define the original filename in 'ChmLoadOptions' to avoid this behavior.
let loadOptions = new aw.Loading.ChmLoadOptions();
loadOptions.originalFileName = "amhelp.chm";

let doc = new aw.Document(base.myDir + "Document with ms-its links.chm", loadOptions);

doc.save(base.artifactsDir + "ExChmLoadOptions.originalFileName.html");
```

### See Also

* module [Aspose.Words.Loading](../../)
* class [ChmLoadOptions](../)

