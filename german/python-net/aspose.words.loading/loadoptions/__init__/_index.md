---
title: LoadOptions constructor
linktitle: LoadOptions constructor
articleTitle: LoadOptions constructor
second_title: Aspose.Words for Python
description: "aspose.words.loading.LoadOptions constructor"
type: docs
weight: 10
url: /de/python-net/aspose.words.loading/loadoptions/__init__/
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
# Aspose.Words wirft eine Ausnahme, wenn wir versuchen, ein verschlüsseltes Dokument ohne dessen Passwort zu öffnen.
with self.assertRaises(Exception):
    doc = aw.Document(file_name=MY_DIR + 'Encrypted.docx')
# Beim Laden eines solchen Dokuments wird das Passwort dem Konstruktor des Dokuments über ein LoadOptions-Objekt übergeben.
options = aw.loading.LoadOptions(password='docPassword')
# Es gibt zwei Möglichkeiten, ein verschlüsseltes Dokument mit einem LoadOptions-Objekt zu laden.
# 1 -  Laden Sie das Dokument vom lokalen Dateisystem über den Dateinamen:
doc = aw.Document(file_name=MY_DIR + 'Encrypted.docx', load_options=options)
# 2 -  Laden Sie das Dokument aus einem Stream:
with system_helper.io.File.open_read(MY_DIR + 'Encrypted.docx') as stream:
    doc = aw.Document(stream=stream, load_options=options)
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
* class [LoadOptions](../)

