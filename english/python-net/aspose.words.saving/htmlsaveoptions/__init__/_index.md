---
title: HtmlSaveOptions constructor
second_title: Aspose.Words for Python via .NET API Reference
description: "aspose.words.saving.HtmlSaveOptions constructor"
type: docs
weight: 10
url: /python-net/aspose.words.saving/htmlsaveoptions/__init__/
---

## HtmlSaveOptions() {#default}

Initializes a new instance of this class that can be used to save a document
in the [SaveFormat.HTML](../../../aspose.words/saveformat/#HTML) format.



```python
def __init__(self):
    ...
```

## HtmlSaveOptions(save_format) {#saveformat}

Initializes a new instance of this class that can be used to save a document
in the [SaveFormat.HTML](../../../aspose.words/saveformat/#HTML), [SaveFormat.MHTML](../../../aspose.words/saveformat/#MHTML)
or [SaveFormat.EPUB](../../../aspose.words/saveformat/#EPUB) format.



```python
def __init__(self, save_format: aspose.words.SaveFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) |  |

## Examples

Shows how to use a specific encoding when saving a document to .epub.

```python
doc = aw.Document(MY_DIR + "Rendering.docx")

# Use a SaveOptions object to specify the encoding for a document that we will save.
save_options = aw.saving.HtmlSaveOptions()
save_options.save_format = aw.SaveFormat.EPUB
save_options.encoding = "utf-8"

# By default, an output .epub document will have all its contents in one HTML part.
# A split criterion allows us to segment the document into several HTML parts.
# We will set the criteria to split the document into heading paragraphs.
# This is useful for readers who cannot read HTML files more significant than a specific size.
save_options.document_split_criteria = aw.saving.DocumentSplitCriteria.HEADING_PARAGRAPH

# Specify that we want to export document properties.
save_options.export_document_properties = True

doc.save(ARTIFACTS_DIR + "HtmlSaveOptions.doc2_epub_save_options.epub", save_options)
```

Shows how to save a document to a specific version of HTML.

```python
doc = aw.Document(MY_DIR + "Rendering.docx")

options = aw.saving.HtmlSaveOptions(aw.SaveFormat.HTML)
options.html_version = html_version
options.pretty_format = True

doc.save(ARTIFACTS_DIR + "HtmlSaveOptions.html_versions.html", options)

# Our HTML documents will have minor differences to be compatible with different HTML versions.
with open(ARTIFACTS_DIR + "HtmlSaveOptions.html_versions.html", "rt", encoding="utf-8") as file:
    out_doc_contents = file.read()

if html_version == aw.saving.HtmlVersion.HTML5:
    self.assertIn(
        "<a id=\"_Toc76372689\"></a>",
        out_doc_contents)
    self.assertIn(
        "<a id=\"_Toc76372689\"></a>",
        out_doc_contents)
    self.assertIn(
        "<table style=\"-aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">",
        out_doc_contents)

elif html_version == aw.saving.HtmlVersion.XHTML:
    self.assertIn(
        "<a name=\"_Toc76372689\"></a>",
        out_doc_contents)
    self.assertIn(
        "<ul type=\"disc\" style=\"margin:0pt; padding-left:0pt\">",
        out_doc_contents)
    self.assertIn(
        "<table cellspacing=\"0\" cellpadding=\"0\" style=\"-aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\"",
        out_doc_contents)
```

## See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

