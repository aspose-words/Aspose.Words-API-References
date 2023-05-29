---
title: LoadFormat enumeration
linktitle: LoadFormat enumeration
articleTitle: LoadFormat enumeration
second_title: Aspose.Words for Python
description: "aspose.words.LoadFormat enumeration. Indicates the format of the document that is to be loaded."
type: docs
weight: 650
url: /python-net/aspose.words/loadformat/
---

## LoadFormat enumeration

Indicates the format of the document that is to be loaded.


### Members

| Name | Description |
| --- | --- |
| AUTO | Instructs Aspose.Words to recognize the format automatically. |
| DOC | Microsoft Word 95 or Word 97 - 2003 Document. |
| DOT | Microsoft Word 95 or Word 97 - 2003 Template. |
| DOC_PRE_WORD60 | The document is in pre-Word 95 format. Aspose.Words does not currently support loading such documents. |
| DOCX | Office Open XML WordprocessingML Document (macro-free). |
| DOCM | Office Open XML WordprocessingML Macro-Enabled Document. |
| DOTX | Office Open XML WordprocessingML Template (macro-free). |
| DOTM | Office Open XML WordprocessingML Macro-Enabled Template. |
| FLAT_OPC | Office Open XML WordprocessingML stored in a flat XML file instead of a ZIP package. |
| FLAT_OPC_MACRO_ENABLED | Office Open XML WordprocessingML Macro-Enabled Document stored in a flat XML file instead of a ZIP package. |
| FLAT_OPC_TEMPLATE | Office Open XML WordprocessingML Template (macro-free) stored in a flat XML file instead of a ZIP package. |
| FLAT_OPC_TEMPLATE_MACRO_ENABLED | Office Open XML WordprocessingML Macro-Enabled Template stored in a flat XML file instead of a ZIP package. |
| RTF | RTF format. |
| WORD_ML | Microsoft Word 2003 WordprocessingML format. |
| HTML | HTML format. |
| MHTML | MHTML (Web archive) format. |
| MOBI | MOBI format. Used by MobiPocket reader and Amazon Kindle readers. |
| CHM | CHM (Compiled HTML Help) format. |
| AZW3 | AZW3 format. Used by Amazon Kindle readers. |
| EPUB | EPUB format. |
| ODT | ODF Text Document. |
| OTT | ODF Text Document Template. |
| TEXT | Plain Text. |
| MARKDOWN | Markdown text document. |
| PDF | Pdf document. |
| XML | XML document. |
| UNKNOWN | Unrecognized format, cannot be loaded by Aspose.Words. |

### Examples

Shows how save a web page as a .docx file.

```python
url = "https://www.aspose.com/"

with io.BytesIO(urlopen(url).read()) as stream:
    # The URL is used again as a "base_uri" to ensure that any relative image paths are retrieved correctly.
    options = aw.loading.LoadOptions(aw.LoadFormat.HTML, "", url)

    # Load the HTML document from stream and pass the LoadOptions object.
    doc = aw.Document(stream, options)

    # At this stage, we can read and edit the document's contents and then save it to the local file system.
    self.assertEqual("HYPERLINK \"https://products.aspose.com/words/family/\" \\o \"Aspose.Words\"",

    doc.save(ARTIFACTS_DIR + "Document.insert_html_from_web_page.docx")
```

Shows how to use the aw.FileFormatUtil methods to detect the format of a document.

```python
# Load a document from a file that is missing a file extension, and then detect its file format.
with open(MY_DIR + "Word document with missing file extension", "rb") as doc_stream:

    info = aw.FileFormatUtil.detect_file_format(doc_stream)
    load_format = info.load_format

    self.assertEqual(aw.LoadFormat.DOC, load_format)

    # Below are two methods of converting a LoadFormat to its corresponding SaveFormat.
    # 1 -  Get the file extension string for the LoadFormat, then get the corresponding SaveFormat from that string:
    file_extension = aw.FileFormatUtil.load_format_to_extension(load_format)
    save_format = aw.FileFormatUtil.extension_to_save_format(file_extension)

    # 2 -  Convert the LoadFormat directly to its SaveFormat:
    save_format = aw.FileFormatUtil.load_format_to_save_format(load_format)

    # Load a document from the stream, and then save it to the automatically detected file extension.
    doc = aw.Document(doc_stream)

    self.assertEqual(".doc", aw.FileFormatUtil.save_format_to_extension(save_format))

    doc.save(ARTIFACTS_DIR + "File.save_to_detected_file_format" + aw.FileFormatUtil.save_format_to_extension(save_format))
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

### See Also

* module [aspose.words](../)

