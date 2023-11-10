---
title: LoadOptions constructor
linktitle: LoadOptions constructor
articleTitle: LoadOptions constructor
second_title: Aspose.Words for Python
description: "aspose.words.loading.LoadOptions constructor"
type: docs
weight: 10
url: /python-net/aspose.words.loading/loadoptions/__init__/
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

Shows how to open an HTML document with images from a stream using a base URI.

```python
with open(MY_DIR + "Document.html", "rb") as stream:
    # Pass the URI of the base folder while loading it
    # so that any images with relative URIs in the HTML document can be found.
    load_options = aw.loading.LoadOptions()
    load_options.base_uri = IMAGE_DIR

    doc = aw.Document(stream, load_options)

    # Verify that the first shape of the document contains a valid image.
    shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()

    self.assertTrue(shape.is_image)
    self.assertIsNotNone(shape.image_data.image_bytes)
    self.assertAlmostEqual(32.0, aw.ConvertUtil.point_to_pixel(shape.width), delta=0.01)
    self.assertAlmostEqual(32.0, aw.ConvertUtil.point_to_pixel(shape.height), delta=0.01)
```

Shows how to load an encrypted Microsoft Word document.

```python
# Aspose.Words throw an exception if we try to open an encrypted document without its password.
with self.assertRaises(Exception):
    doc = aw.Document(MY_DIR + "Encrypted.docx")

# When loading such a document, the password is passed to the document's constructor using a LoadOptions object.
options = aw.loading.LoadOptions("docPassword")

# There are two ways of loading an encrypted document with a LoadOptions object.
# 1 -  Load the document from the local file system by filename:
doc = aw.Document(MY_DIR + "Encrypted.docx", options)

# 2 -  Load the document from a stream:
with open(MY_DIR + "Encrypted.docx", "rb") as stream:
    doc = aw.Document(stream, options)
```

Shows how save a web page as a .docx file.

```python
url = "https://www.aspose.com/"

with io.BytesIO(urlopen(url).read()) as stream:
    # The URL is used again as a "base_uri" to ensure that any relative image paths are retrieved correctly.
    options = aw.loading.LoadOptions(aw.LoadFormat.HTML, "", url)

    # Load the HTML document from stream and pass the LoadOptions object.
    doc = aw.Document(stream, options)

    # At this stage, we can read and edit the document's contents and then save it to the local file system.

    doc.save(ARTIFACTS_DIR + "Document.insert_html_from_web_page.docx")
```

Shows how to specify a base URI when opening an html document.

```python
# Suppose we want to load an .html document that contains an image linked by a relative URI
# while the image is in a different location. In that case, we will need to resolve the relative URI into an absolute one.
# We can provide a base URI using an HtmlLoadOptions object.
load_options = aw.loading.HtmlLoadOptions(aw.LoadFormat.HTML, "", IMAGE_DIR)

self.assertEqual(aw.LoadFormat.HTML, load_options.load_format)

doc = aw.Document(MY_DIR + "Missing image.html", load_options)

# While the image was broken in the input .html, our custom base URI helped us repair the link.
image_shape = doc.get_child_nodes(aw.NodeType.SHAPE, True)[0].as_shape()
self.assertTrue(image_shape.is_image)

# This output document will display the image that was missing.
doc.save(ARTIFACTS_DIR + "HtmlLoadOptions.base_uri.docx")
```

## See Also

* module [aspose.words.loading](../../)
* class [LoadOptions](../)

