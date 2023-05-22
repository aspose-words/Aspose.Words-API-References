---
title: HtmlLoadOptions constructor
linktitle: HtmlLoadOptions constructor
articleTitle: HtmlLoadOptions constructor
second_title: Aspose.Words for Python
description: "aspose.words.loading.HtmlLoadOptions constructor"
type: docs
weight: 10
url: /python-net/aspose.words.loading/htmlloadoptions/__init__/
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
| password | str |  |

## HtmlLoadOptions(load_format, password, base_uri) {#loadformat_str_str}

A shortcut to initialize a new instance of this class with properties set to the specified values.


```python
def __init__(self, load_format: aspose.words.LoadFormat, password: str, base_uri: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| load_format | [LoadFormat](../../../aspose.words/loadformat/) |  |
| password | str |  |
| base_uri | str |  |

## Examples

Shows how to support conditional comments while loading an HTML document.

```python
load_options = aw.loading.HtmlLoadOptions()

# If the value is True, then we take VML code into account while parsing the loaded document.
load_options.support_vml = support_vml

# This document contains a JPEG image within "<!--[if gte vml 1]>" tags,
# and a different PNG image within "<![if !vml]>" tags.
# If we set the "support_vml" flag to "True", then Aspose.Words will load the JPEG.
# If we set this flag to "False", then Aspose.Words will only load the PNG.
doc = aw.Document(MY_DIR + "VML conditional.htm", load_options)

if support_vml:
    self.assertEqual(aw.drawing.ImageType.JPEG, doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape().image_data.image_type)
else:
    self.assertEqual(aw.drawing.ImageType.PNG, doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape().image_data.image_type)
```

Shows how to encrypt an Html document, and then open it using a password.

```python
# Create and sign an encrypted HTML document from an encrypted .docx.
certificate_holder = aw.digitalsignatures.CertificateHolder.create(MY_DIR + "morzal.pfx", "aw")

sign_options = aw.digitalsignatures.SignOptions()
sign_options.comments = "Comment"
sign_options.sign_time = datetime.now()
sign_options.decryption_password = "docPassword"

input_file_name = MY_DIR + "Encrypted.docx"
output_file_name = ARTIFACTS_DIR + "HtmlLoadOptions.encrypted_html.html"
aw.digitalsignatures.DigitalSignatureUtil.sign(input_file_name, output_file_name, certificate_holder, sign_options)

# To load and read this document, we will need to pass its decryption
# password using a HtmlLoadOptions object.
load_options = aw.loading.HtmlLoadOptions("docPassword")

self.assertEqual(sign_options.decryption_password, load_options.password)

doc = aw.Document(output_file_name, load_options)

self.assertEqual("Test encrypted document.", doc.get_text().strip())
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
* class [HtmlLoadOptions](../)

