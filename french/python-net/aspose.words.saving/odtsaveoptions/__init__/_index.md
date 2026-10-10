---
title: OdtSaveOptions constructor
linktitle: OdtSaveOptions constructor
articleTitle: OdtSaveOptions constructor
second_title: Aspose.Words for Python
description: "aspose.words.saving.OdtSaveOptions constructor"
type: docs
weight: 10
url: /fr/python-net/aspose.words.saving/odtsaveoptions/__init__/
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

Shows how to encrypt a saved ODT/OTT document with a password, and then load it using Aspose.Words.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
# Créez un nouveau OdtSaveOptions et transmettez soit "SaveFormat.Odt",
# ou "SaveFormat.Ott" comme format dans lequel enregistrer le document.
save_options = aw.saving.OdtSaveOptions(save_format=save_format)
save_options.password = '@sposeEncrypted_1145'
extension_string = aw.FileFormatUtil.save_format_to_extension(save_format)
# Si nous ouvrons ce document avec un éditeur approprié,
# il nous demandera le mot de passe que nous avons spécifié dans l'objet SaveOptions.
doc.save(file_name=ARTIFACTS_DIR + 'OdtSaveOptions.Encrypt' + extension_string, save_options=save_options)
doc_info = aw.FileFormatUtil.detect_file_format(file_name=ARTIFACTS_DIR + 'OdtSaveOptions.Encrypt' + extension_string)
self.assertTrue(doc_info.is_encrypted)
# Si nous souhaitons ouvrir ou modifier à nouveau ce document en utilisant Aspose.Words,
# nous devrons fournir un objet LoadOptions contenant le mot de passe correct au constructeur de chargement.
doc = aw.Document(file_name=ARTIFACTS_DIR + 'OdtSaveOptions.Encrypt' + extension_string, load_options=aw.loading.LoadOptions(password='@sposeEncrypted_1145'))
self.assertEqual('Hello world!', doc.get_text().strip())
```

## See Also

* module [aspose.words.saving](../../)
* class [OdtSaveOptions](../)

