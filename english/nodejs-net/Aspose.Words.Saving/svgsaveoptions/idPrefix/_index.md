---
title: SvgSaveOptions.idPrefix property
linktitle: idPrefix property
articleTitle: idPrefix property
second_title: Aspose.Words for Node.js
description: "SvgSaveOptions.idPrefix property. Specifies a prefix that is prepended to all generated element IDs in the output document"
type: docs
weight: 40
url: /nodejs-net/aspose.words.saving/svgsaveoptions/idPrefix/
---

## SvgSaveOptions.idPrefix property

Specifies a prefix that is prepended to all generated element IDs in the output document.
Default value is null and no prefix is prepended.


```js
get idPrefix(): string
```

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentException)) | The value does not meet the requirements specified above. |

### Remarks

If the prefix is specified, it can contain only letters, digits, underscores, and hyphens,
and must start with a letter.


### Examples

Shows how to add a prefix that is prepended to all generated element IDs (svg).

```js
let doc = new aw.Document(base.myDir + "Id prefix.docx");

let saveOptions = new aw.Saving.SvgSaveOptions();
saveOptions.idPrefix = "pfx1_";

doc.save(base.artifactsDir + "SvgSaveOptions.IdPrefixSvg.html", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [SvgSaveOptions](../)

