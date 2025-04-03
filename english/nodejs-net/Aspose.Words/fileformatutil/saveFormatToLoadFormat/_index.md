---
title: FileFormatUtil.saveFormatToLoadFormat method
linktitle: saveFormatToLoadFormat method
articleTitle: saveFormatToLoadFormat method
second_title: Aspose.Words for NodeJs
description: "FileFormatUtil.saveFormatToLoadFormat method. Converts a [SaveFormat](../../saveformat/) value to a [LoadFormat](../../loadformat/) value if possible."
type: docs
weight: 90
url: /nodejs-net/aspose.words/fileformatutil/saveFormatToLoadFormat/
---

## saveFormatToLoadFormat(saveFormat) {#saveformat}

Converts a [SaveFormat](../../saveformat/) value to a [LoadFormat](../../loadformat/) value if possible.



```js
saveFormatToLoadFormat(saveFormat: Aspose.Words.SaveFormat)
```

| Parameter | Type | Description |
| --- | --- | --- |
| saveFormat | [SaveFormat](../../saveformat/) |  |

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentException)) | Throws when cannot convert. |

### Examples

Shows how to convert a save format to its corresponding load format.

```js
expect(aw.FileFormatUtil.saveFormatToLoadFormat(aw.SaveFormat.Html)).toEqual(aw.LoadFormat.Html);

// Some file types can have documents saved to, but not loaded from using Aspose.words.
// If we attempt to convert a save format of such a type to a load format, an exception will be thrown.
expect(() => aw.FileFormatUtil.saveFormatToLoadFormat(aw.SaveFormat.Jpeg)).toThrow("Cannot convert this save format to a load format.");
```

### See Also

* module [Aspose.Words](../../)
* class [FileFormatUtil](../)

