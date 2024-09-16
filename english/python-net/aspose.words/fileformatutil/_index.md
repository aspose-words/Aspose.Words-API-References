---
title: FileFormatUtil class
linktitle: FileFormatUtil class
articleTitle: FileFormatUtil class
second_title: Aspose.Words for Python
description: "aspose.words.FileFormatUtil class. Provides utility methods for working with file formats, such as detecting file format or converting file extensions to/from file format enums"
type: docs
weight: 420
url: /python-net/aspose.words/fileformatutil/
---

## FileFormatUtil class

Provides utility methods for working with file formats, such as detecting file format
or converting file extensions to/from file format enums.
To learn more, visit the [Detect File Format and Check Format Compatibility](https://docs.aspose.com/words/python-net/detect-file-format-and-check-format-compatibility/) documentation article.




### Methods

| Name | Description |
| --- | --- |
|[ content_type_to_load_format(content_type)](./content_type_to_load_format/#str) | Converts IANA content type into a load format enumerated value. |
|[ content_type_to_save_format(content_type)](./content_type_to_save_format/#str) | Converts IANA content type into a save format enumerated value. |
|[ detect_file_format(file_name)](./detect_file_format/#str) | Detects and returns the information about a format of a document stored in a disk file. |
|[ detect_file_format(stream)](./detect_file_format/#bytesio) | Detects and returns the information about a format of a document stored in a stream. |
|[ extension_to_save_format(extension)](./extension_to_save_format/#str) | Converts a file name extension into a [SaveFormat](../saveformat/) value. |
|[ image_type_to_extension(image_type)](./image_type_to_extension/#imagetype) | Converts an Aspose.Words image type enumerated value into a file extension. The returned extension is a lower-case string with a leading dot. |
|[ load_format_to_extension(load_format)](./load_format_to_extension/#loadformat) | Converts a load format enumerated value into a file extension. The returned extension is a lower-case string with a leading dot. |
|[ load_format_to_save_format(load_format)](./load_format_to_save_format/#loadformat) | Converts a [LoadFormat](../loadformat/) value to a [SaveFormat](../saveformat/) value if possible. |
|[ save_format_to_extension(save_format)](./save_format_to_extension/#saveformat) | Converts a save format enumerated value into a file extension. The returned extension is a lower-case string with a leading dot. |
|[ save_format_to_load_format(save_format)](./save_format_to_load_format/#saveformat) | Converts a [SaveFormat](../saveformat/) value to a [LoadFormat](../loadformat/) value if possible. |

### Examples

Shows how to detect encoding in an html file.

```python
info = aw.FileFormatUtil.detect_file_format(MY_DIR + 'Document.html')
self.assertEqual(aw.LoadFormat.HTML, info.load_format)
# The "encoding" property is used only when we create a FileFormatInfo object for an html document.
self.assertEqual('windows-1252', info.encoding)
```

### See Also

* module [aspose.words](../)

