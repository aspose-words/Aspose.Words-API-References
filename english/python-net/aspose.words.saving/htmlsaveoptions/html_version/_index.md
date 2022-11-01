---
title: html_version property
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies version of HTML standard that should be used when saving the document to HTML or MHTML"
type: docs
weight: 340
url: /python-net/aspose.words.saving/htmlsaveoptions/html_version/
---

## HtmlSaveOptions.html_version property

Specifies version of HTML standard that should be used when saving the document to HTML or MHTML.
Default value is [HtmlVersion.XHTML](../../htmlversion/#XHTML).



### Examples

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

Shows how to display a DOCTYPE heading when converting documents to the Xhtml 1.0 transitional standard.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.writeln("Hello world!")

options = aw.saving.HtmlSaveOptions(aw.SaveFormat.HTML)
options.html_version = aw.saving.HtmlVersion.XHTML
options.export_xhtml_transitional = show_doctype_declaration
options.pretty_format = True

doc.save(ARTIFACTS_DIR + "HtmlSaveOptions.export_xhtml_transitional.html", options)

# Our document will only contain a DOCTYPE declaration heading if we have set the "export_xhtml_transitional" flag to "True".
with open(ARTIFACTS_DIR + "HtmlSaveOptions.export_xhtml_transitional.html", "rt", encoding="utf-8") as file:
    out_doc_contents = file.read()

if show_doctype_declaration:
    self.assertIn(
        "<?xml version=\"1.0\" encoding=\"utf-8\" standalone=\"no\"?>\n" +
        "<!DOCTYPE html PUBLIC \"-//W3C//DTD XHTML 1.0 Transitional//EN\" \"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd\">\n" +
        "<html xmlns=\"http://www.w3.org/1999/xhtml\">",
        out_doc_contents)
else:
    self.assertIn("<html>", out_doc_contents)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

