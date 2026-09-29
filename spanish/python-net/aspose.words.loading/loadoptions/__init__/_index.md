---
title: LoadOptions constructor
linktitle: LoadOptions constructor
articleTitle: LoadOptions constructor
second_title: Aspose.Words for Python
description: "aspose.words.loading.LoadOptions constructor"
type: docs
weight: 10
url: /es/python-net/aspose.words.loading/loadoptions/__init__/
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
# Aspose.Words lanza una excepción si intentamos abrir un documento cifrado sin su contraseña.
with self.assertRaises(Exception):
    doc = aw.Document(file_name=MY_DIR + 'Encrypted.docx')
# Al cargar dicho documento, la contraseña se pasa al constructor del documento usando un objeto LoadOptions.
options = aw.loading.LoadOptions(password='docPassword')
# Hay dos formas de cargar un documento cifrado con un objeto LoadOptions.
# 1 -  Cargue el documento desde el sistema de archivos local mediante el nombre de archivo:
doc = aw.Document(file_name=MY_DIR + 'Encrypted.docx', load_options=options)
# 2 -  Cargue el documento desde un flujo:
with system_helper.io.File.open_read(MY_DIR + 'Encrypted.docx') as stream:
    doc = aw.Document(stream=stream, load_options=options)
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
* class [LoadOptions](../)

