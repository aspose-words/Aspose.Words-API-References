---
title: OdtSaveOptions constructor
linktitle: OdtSaveOptions constructor
articleTitle: OdtSaveOptions constructor
second_title: Aspose.Words for Python
description: "aspose.words.saving.OdtSaveOptions constructor"
type: docs
weight: 10
url: /python-net/aspose.words.saving/odtsaveoptions/__init__/
---

## OdtSaveOptions() {#default}

Initializes a new instance of this class that can be used to save a document in the [SaveFormat.ODT](../../../aspose.words/saveformat/#ODT) format.



```python
def __init__(self):
    ...
```

## OdtSaveOptions(password) {#str}

Initializes a new instance of this class that can be used to save a document in the [SaveFormat.ODT](../../../aspose.words/saveformat/#ODT) format
encrypted with a password.



```python
def __init__(self, password: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| password | str |  |

## OdtSaveOptions(save_format) {#saveformat}

Initializes a new instance of this class that can be used to save a document in the [SaveFormat.ODT](../../../aspose.words/saveformat/#ODT) or
[SaveFormat.OTT](../../../aspose.words/saveformat/#OTT) format.



```python
def __init__(self, save_format: aspose.words.SaveFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) | Can be [SaveFormat.ODT](../../../aspose.words/saveformat/#ODT) or [SaveFormat.OTT](../../../aspose.words/saveformat/#OTT). |

## Examples

Shows how to make a saved document conform to an older ODT schema.

```python
doc = aw.Document(MY_DIR + 'Rendering.docx')
save_options = aw.saving.OdtSaveOptions()
save_options.measure_unit = aw.saving.OdtSaveMeasureUnit.CENTIMETERS
save_options.is_strict_schema11 = export_to_odt11_specs
doc.save(ARTIFACTS_DIR + 'OdtSaveOptions.odt11_schema.odt', save_options)
```

Shows how to encrypt a saved ODT/OTT document with a password, and then load it using Aspose.Words.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.writeln('Hello world!')
# Create a new OdtSaveOptions, and pass either "SaveFormat.ODT",
# or "SaveFormat.OTT" as the format to save the document in.
save_options = aw.saving.OdtSaveOptions(save_format)
save_options.password = '@sposeEncrypted_1145'
extension_string = aw.FileFormatUtil.save_format_to_extension(save_format)
# If we open this document with an appropriate editor,
# it will prompt us for the password we specified in the SaveOptions object.
doc.save(ARTIFACTS_DIR + 'OdtSaveOptions.encrypt' + extension_string, save_options)
doc_info = aw.FileFormatUtil.detect_file_format(ARTIFACTS_DIR + 'OdtSaveOptions.encrypt' + extension_string)
self.assertTrue(doc_info.is_encrypted)
# If we wish to open or edit this document again using Aspose.Words,
# we will have to provide a LoadOptions object with the correct password to the loading constructor.
doc = aw.Document(ARTIFACTS_DIR + 'OdtSaveOptions.encrypt' + extension_string, aw.loading.LoadOptions('@sposeEncrypted_1145'))
self.assertEqual('Hello world!', doc.get_text().strip())
```

## See Also

* module [aspose.words.saving](../../)
* class [OdtSaveOptions](../)

