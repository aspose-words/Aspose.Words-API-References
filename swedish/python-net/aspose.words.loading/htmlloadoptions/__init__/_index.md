---
title: HtmlLoadOptions constructor
linktitle: HtmlLoadOptions constructor
articleTitle: HtmlLoadOptions constructor
second_title: Aspose.Words for Python
description: "aspose.words.loading.HtmlLoadOptions constructor"
type: docs
weight: 10
url: /sv/python-net/aspose.words.loading/htmlloadoptions/__init__/
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
# Skapa och signera ett krypterat HTML-dokument från en krypterad .docx.
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + 'morzal.pfx', password='aw')
sign_options = aw.digitalsignatures.SignOptions()
sign_options.comments = 'Comment'
sign_options.sign_time = datetime.datetime.now()
sign_options.decryption_password = 'docPassword'
input_file_name = MY_DIR + 'Encrypted.docx'
output_file_name = ARTIFACTS_DIR + 'HtmlLoadOptions.EncryptedHtml.html'
aw.digitalsignatures.DigitalSignatureUtil.sign(src_file_name=input_file_name, dst_file_name=output_file_name, cert_holder=certificate_holder, sign_options=sign_options)
# För att läsa in och läsa detta dokument måste vi skicka dess dekryptering
# lösenord med ett HtmlLoadOptions-objekt.
load_options = aw.loading.HtmlLoadOptions(password='docPassword')
self.assertEqual(sign_options.decryption_password, load_options.password)
doc = aw.Document(file_name=output_file_name, load_options=load_options)
self.assertEqual('Test encrypted document.', doc.get_text().strip())
```

Shows how to specify a base URI when opening an html document.

```python
# Anta att vi vill läsa in ett .html‑dokument som innehåller en bild länkad med en relativ URI
# medan bilden finns på en annan plats. I så fall måste vi lösa upp den relativa URI:n till en absolut.
# Vi kan ange en bas‑URI med ett HtmlLoadOptions‑objekt.
load_options = aw.loading.HtmlLoadOptions(load_format=aw.LoadFormat.HTML, password='', base_uri=IMAGE_DIR)
self.assertEqual(aw.LoadFormat.HTML, load_options.load_format)
doc = aw.Document(file_name=MY_DIR + 'Missing image.html', load_options=load_options)
# Även om bilden var trasig i indata‑.html hjälpte vår anpassade bas‑URI oss att reparera länken.
image_shape = doc.get_child_nodes(aw.NodeType.SHAPE, True)[0].as_shape()
self.assertTrue(image_shape.is_image)
# Detta utdata‑dokument kommer att visa bilden som saknades.
doc.save(file_name=ARTIFACTS_DIR + 'HtmlLoadOptions.BaseUri.docx')
```

## See Also

* module [aspose.words.loading](../../)
* class [HtmlLoadOptions](../)

