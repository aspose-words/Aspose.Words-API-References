---
title: FileFormatUtil class
linktitle: FileFormatUtil class
articleTitle: FileFormatUtil class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.FileFormatUtil class. Provides utility methods for working with file formats, such as detecting file format or converting file extensions to/from file format enums"
type: docs
weight: 430
url: /nodejs-net/aspose.words/fileformatutil/
---

## FileFormatUtil class

Provides utility methods for working with file formats, such as detecting file format
or converting file extensions to/from file format enums.
To learn more, visit the [Detect File Format and Check Format Compatibility](https://docs.aspose.com/words/nodejs-net/detect-file-format-and-check-format-compatibility/) documentation article.




### Methods

| Name | Description |
| --- | --- |
|[ contentTypeToLoadFormat(contentType)](./contentTypeToLoadFormat/#string) | Converts IANA content type into a load format enumerated value. |
|[ contentTypeToSaveFormat(contentType)](./contentTypeToSaveFormat/#string) | Converts IANA content type into a save format enumerated value. |
|[ detectFileFormat(fileName)](./detectFileFormat/#string) | Detects and returns the information about a format of a document stored in a disk file. |
|[ detectFileFormat(stream)](./detectFileFormat/#buffer) | Detects and returns the information about a format of a document stored in a stream. |
|[ extensionToSaveFormat(extension)](./extensionToSaveFormat/#string) | Converts a file name extension into a [SaveFormat](../saveformat/) value. |
|[ imageTypeToExtension(imageType)](./imageTypeToExtension/#imagetype) | Converts an Aspose.Words image type enumerated value into a file extension. The returned extension is a lower-case string with a leading dot. |
|[ loadFormatToExtension(loadFormat)](./loadFormatToExtension/#loadformat) | Converts a load format enumerated value into a file extension. The returned extension is a lower-case string with a leading dot. |
|[ loadFormatToSaveFormat(loadFormat)](./loadFormatToSaveFormat/#loadformat) | Converts a [LoadFormat](../loadformat/) value to a [SaveFormat](../saveformat/) value if possible. |
|[ saveFormatToExtension(saveFormat)](./saveFormatToExtension/#saveformat) | Converts a save format enumerated value into a file extension. The returned extension is a lower-case string with a leading dot. |
|[ saveFormatToLoadFormat(saveFormat)](./saveFormatToLoadFormat/#saveformat) | Converts a [SaveFormat](../saveformat/) value to a [LoadFormat](../loadformat/) value if possible. |

### Examples

Shows how to detect encoding in an html file.

```js
let info = aw.FileFormatUtil.detectFileFormat(base.myDir + "Document.html");

expect(info.loadFormat).toEqual(aw.LoadFormat.Html);

// The Encoding property is used only when we create a FileFormatInfo object for an html document.
expect(info.encoding).toEqual("windows-1252");
```

### See Also

* module [Aspose.Words](../)

