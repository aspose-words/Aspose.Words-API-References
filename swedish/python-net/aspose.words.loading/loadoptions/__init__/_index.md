---
title: LoadOptions constructor
linktitle: LoadOptions constructor
articleTitle: LoadOptions constructor
second_title: Aspose.Words for Python
description: "aspose.words.loading.LoadOptions constructor"
type: docs
weight: 10
url: /sv/python-net/aspose.words.loading/loadoptions/__init__/
---

## LoadOptions() {#default}

Initializes a new instance of this class with default values.


```python
def __init__(self):
    ...
```

## LoadOptions(password) {#str}

A shortcut to initialize a new instance of this class with the specified password to load an encrypted document.


```python
def __init__(self, password: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| password | str | The password to open an encrypted document. Can be ``None`` or empty string. |

## LoadOptions(load_format, password, base_uri) {#loadformat_str_str}

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

Shows how to load an encrypted Microsoft Word document.

```python
doc = None
# Aspose.Words kastar ett undantag om vi försöker öppna ett krypterat dokument utan dess lösenord.
with self.assertRaises(Exception):
    doc = aw.Document(file_name=MY_DIR + 'Encrypted.docx')
# När ett sådant dokument laddas, skickas lösenordet till dokumentets konstruktor med ett LoadOptions-objekt.
options = aw.loading.LoadOptions(password='docPassword')
# Det finns två sätt att ladda ett krypterat dokument med ett LoadOptions-objekt.
# 1 -  Ladda dokumentet från det lokala filsystemet med filnamn:
doc = aw.Document(file_name=MY_DIR + 'Encrypted.docx', load_options=options)
# 2 -  Ladda dokumentet från en ström:
with system_helper.io.File.open_read(MY_DIR + 'Encrypted.docx') as stream:
    doc = aw.Document(stream=stream, load_options=options)
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
* class [LoadOptions](../)

