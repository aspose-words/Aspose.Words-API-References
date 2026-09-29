---
title: HtmlLoadOptions constructor
linktitle: HtmlLoadOptions constructor
articleTitle: HtmlLoadOptions constructor
second_title: Aspose.Words for Python
description: "aspose.words.loading.HtmlLoadOptions constructor"
type: docs
weight: 10
url: /es/python-net/aspose.words.loading/htmlloadoptions/__init__/
---

## HtmlLoadOptions() {#default}

Initializes a new instance of this class with default values.


```python
def __init__(self):
    ...
```

## HtmlLoadOptions(password) {#str}

A shortcut to initialize a new instance of this class with the specified password to load an encrypted document.


```python
def __init__(self, password: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| password | str | The password to open an encrypted document. Can be ``None`` or empty string. |

## HtmlLoadOptions(load_format, password, base_uri) {#loadformat_str_str}

A shortcut to initialize a new instance of this class with properties set to the specified values.


```python
def __init__(self, load_format: aspose.words.LoadFormat, password: str, base_uri: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| load_format | [LoadFormat](../../../aspose.words/loadformat/) | The format of the document to be loaded. |
| password | str | The password to open an encrypted document. Can be ``None`` or empty string. |
| base_uri | str | The string that will be used to resolve relative URIs to absolute. Can be ``None`` or empty string. |

## Examples

Shows how to encrypt an Html document, and then open it using a password.

```python
# Cree y firme un documento HTML cifrado a partir de un .docx cifrado.
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + 'morzal.pfx', password='aw')
sign_options = aw.digitalsignatures.SignOptions()
sign_options.comments = 'Comment'
sign_options.sign_time = datetime.datetime.now()
sign_options.decryption_password = 'docPassword'
input_file_name = MY_DIR + 'Encrypted.docx'
output_file_name = ARTIFACTS_DIR + 'HtmlLoadOptions.EncryptedHtml.html'
aw.digitalsignatures.DigitalSignatureUtil.sign(src_file_name=input_file_name, dst_file_name=output_file_name, cert_holder=certificate_holder, sign_options=sign_options)
# Para cargar y leer este documento, necesitaremos proporcionar su descifrado
# contraseña usando un objeto HtmlLoadOptions.
load_options = aw.loading.HtmlLoadOptions(password='docPassword')
self.assertEqual(sign_options.decryption_password, load_options.password)
doc = aw.Document(file_name=output_file_name, load_options=load_options)
self.assertEqual('Test encrypted document.', doc.get_text().strip())
```

Shows how to specify a base URI when opening an html document.

```python
# Supongamos que queremos cargar un documento .html que contiene una imagen vinculada mediante una URI relativa
# mientras que la imagen está en una ubicación diferente. En ese caso, necesitaremos resolver la URI relativa en una absoluta.
# Podemos proporcionar una URI base usando un objeto HtmlLoadOptions.
load_options = aw.loading.HtmlLoadOptions(load_format=aw.LoadFormat.HTML, password='', base_uri=IMAGE_DIR)
self.assertEqual(aw.LoadFormat.HTML, load_options.load_format)
doc = aw.Document(file_name=MY_DIR + 'Missing image.html', load_options=load_options)
# Aunque la imagen estaba rota en el .html de entrada, nuestra URI base personalizada nos ayudó a reparar el enlace.
image_shape = doc.get_child_nodes(aw.NodeType.SHAPE, True)[0].as_shape()
self.assertTrue(image_shape.is_image)
# Este documento de salida mostrará la imagen que faltaba.
doc.save(file_name=ARTIFACTS_DIR + 'HtmlLoadOptions.BaseUri.docx')
```

## See Also

* module [aspose.words.loading](../../)
* class [HtmlLoadOptions](../)

