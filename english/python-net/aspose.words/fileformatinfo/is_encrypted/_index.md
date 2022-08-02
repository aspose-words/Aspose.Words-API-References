---
title: is_encrypted property
second_title: Aspose.Words for Python via .NET API Reference
description: "Returns true if the document is encrypted and requires a password to open."
type: docs
weight: 30
url: /python-net/aspose.words/fileformatinfo/is_encrypted/
---

## FileFormatInfo.is_encrypted property

Returns true if the document is encrypted and requires a password to open.

This property exists to help you sort documents that are encrypted from those that are not.
If you attempt to load an encrypted document using Aspose.Words without supplying a password an 
exception will be thrown. You can use this property to detect whether a document requires a password 
and take some action before loading a document, for example, prompt the user for a password.




### Examples

Shows how to use the aw.FileFormatUtil class to detect the document format and encryption.

```python
doc = aw.Document()

# Configure a SaveOptions object to encrypt the document
# with a password when we save it, and then save the document.
save_options = aw.saving.OdtSaveOptions(aw.SaveFormat.ODT)
save_options.password = "MyPassword"

doc.save(ARTIFACTS_DIR + "File.detect_document_encryption.odt", save_options)

# Verify the file type of our document, and its encryption status.
info = aw.FileFormatUtil.detect_file_format(ARTIFACTS_DIR + "File.detect_document_encryption.odt")

self.assertEqual(".odt", aw.FileFormatUtil.load_format_to_extension(info.load_format))
self.assertTrue(info.is_encrypted)
```

### See Also

* module [aspose.words](../../)
* class [FileFormatInfo](../)
* property [FileFormatInfo.load_format](../load_format/)

