---
title: HtmlLoadOptions constructor
linktitle: HtmlLoadOptions constructor
articleTitle: HtmlLoadOptions constructor
second_title: Aspose.Words for Python
description: "aspose.words.loading.HtmlLoadOptions constructor"
type: docs
weight: 10
url: /de/python-net/aspose.words.loading/htmlloadoptions/__init__/
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
# Erstellen und signieren Sie ein verschlüsseltes HTML-Dokument aus einer verschlüsselten .docx.
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + 'morzal.pfx', password='aw')
sign_options = aw.digitalsignatures.SignOptions()
sign_options.comments = 'Comment'
sign_options.sign_time = datetime.datetime.now()
sign_options.decryption_password = 'docPassword'
input_file_name = MY_DIR + 'Encrypted.docx'
output_file_name = ARTIFACTS_DIR + 'HtmlLoadOptions.EncryptedHtml.html'
aw.digitalsignatures.DigitalSignatureUtil.sign(src_file_name=input_file_name, dst_file_name=output_file_name, cert_holder=certificate_holder, sign_options=sign_options)
# Um dieses Dokument zu laden und zu lesen, müssen wir seine Entschlüsselung übergeben
# Passwort mithilfe eines HtmlLoadOptions-Objekts.
load_options = aw.loading.HtmlLoadOptions(password='docPassword')
self.assertEqual(sign_options.decryption_password, load_options.password)
doc = aw.Document(file_name=output_file_name, load_options=load_options)
self.assertEqual('Test encrypted document.', doc.get_text().strip())
```

Shows how to specify a base URI when opening an html document.

```python
# Angenommen, wir möchten ein .html-Dokument laden, das ein Bild enthält, das über einen relativen URI verlinkt ist
# während sich das Bild an einem anderen Ort befindet. In diesem Fall müssen wir den relativen URI in einen absoluten URI auflösen.
# Wir können mithilfe eines HtmlLoadOptions-Objekts eine Basis-URI bereitstellen.
load_options = aw.loading.HtmlLoadOptions(load_format=aw.LoadFormat.HTML, password='', base_uri=IMAGE_DIR)
self.assertEqual(aw.LoadFormat.HTML, load_options.load_format)
doc = aw.Document(file_name=MY_DIR + 'Missing image.html', load_options=load_options)
# Obwohl das Bild im Eingabe-.html beschädigt war, hat unsere benutzerdefinierte Basis-URI uns geholfen, den Link zu reparieren.
image_shape = doc.get_child_nodes(aw.NodeType.SHAPE, True)[0].as_shape()
self.assertTrue(image_shape.is_image)
# Dieses Ausgabedokument wird das fehlende Bild anzeigen.
doc.save(file_name=ARTIFACTS_DIR + 'HtmlLoadOptions.BaseUri.docx')
```

## See Also

* module [aspose.words.loading](../../)
* class [HtmlLoadOptions](../)

