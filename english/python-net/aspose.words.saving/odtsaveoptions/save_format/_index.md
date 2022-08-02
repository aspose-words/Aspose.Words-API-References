---
title: save_format property
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 50
url: /python-net/aspose.words.saving/odtsaveoptions/save_format/
---

## OdtSaveOptions.save_format property

Specifies the format in which the document will be saved if this save options object is used.
Can be [SaveFormat.ODT](../../../aspose.words/saveformat/#ODT) or [SaveFormat.OTT](../../../aspose.words/saveformat/#OTT).



### Examples

Shows how to encrypt a saved ODT/OTT document with a password, and then load it using Aspose.Words.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.writeln("Hello world!")

# Create a new OdtSaveOptions, and pass either "SaveFormat.ODT",
# or "SaveFormat.OTT" as the format to save the document in.
save_options = aw.saving.OdtSaveOptions(save_format)
save_options.password = "@sposeEncrypted_1145"

extension_string = aw.FileFormatUtil.save_format_to_extension(save_format)

# If we open this document with an appropriate editor,
# it will prompt us for the password we specified in the SaveOptions object.
doc.save(ARTIFACTS_DIR + "OdtSaveOptions.encrypt" + extension_string, save_options)

doc_info = aw.FileFormatUtil.detect_file_format(ARTIFACTS_DIR + "OdtSaveOptions.encrypt" + extension_string)

self.assertTrue(doc_info.is_encrypted)

# If we wish to open or edit this document again using Aspose.Words,
# we will have to provide a LoadOptions object with the correct password to the loading constructor.
doc = aw.Document(ARTIFACTS_DIR + "OdtSaveOptions.encrypt" + extension_string,
    aw.loading.LoadOptions("@sposeEncrypted_1145"))

self.assertEqual("Hello world!", doc.get_text().strip())
```

### See Also

* module [aspose.words.saving](../../)
* class [OdtSaveOptions](../)

