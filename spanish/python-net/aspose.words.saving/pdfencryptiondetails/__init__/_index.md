---
title: PdfEncryptionDetails constructor
linktitle: PdfEncryptionDetails constructor
articleTitle: PdfEncryptionDetails constructor
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfEncryptionDetails constructor"
type: docs
weight: 10
url: /es/python-net/aspose.words.saving/pdfencryptiondetails/__init__/
---

## PdfEncryptionDetails(user_password, owner_password) {#str_str}

Initializes an instance of this class.


```python
def __init__(self, user_password: str, owner_password: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| user_password | str |  |
| owner_password | str |  |

## PdfEncryptionDetails(user_password, owner_password, permissions) {#str_str_pdfpermissions}

Initializes an instance of this class.


```python
def __init__(self, user_password: str, owner_password: str, permissions: aspose.words.saving.PdfPermissions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| user_password | str |  |
| owner_password | str |  |
| permissions | [PdfPermissions](../../pdfpermissions/) |  |

## Examples

Shows how to set permissions on a saved PDF document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
# Amplíe los permisos para permitir la edición de anotaciones.
encryption_details = aw.saving.PdfEncryptionDetails(user_password='password', owner_password='', permissions=aw.saving.PdfPermissions.MODIFY_ANNOTATIONS | aw.saving.PdfPermissions.DOCUMENT_ASSEMBLY)
# Cree un objeto "PdfSaveOptions" que podamos pasar al método "Save" del documento
# para modificar cómo ese método convierte el documento a .PDF.
save_options = aw.saving.PdfSaveOptions()
# Habilite el cifrado mediante la propiedad "EncryptionDetails".
save_options.encryption_details = encryption_details
# Cuando abramos este documento, necesitaremos proporcionar la contraseña antes de acceder a su contenido.
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.EncryptionPermissions.pdf', save_options=save_options)
```

## See Also

* module [aspose.words.saving](../../)
* class [PdfEncryptionDetails](../)

