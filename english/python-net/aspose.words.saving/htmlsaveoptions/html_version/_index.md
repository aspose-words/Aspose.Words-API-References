---
title: HtmlSaveOptions.html_version property
linktitle: html_version property
articleTitle: html_version property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.html_version property. Specifies version of HTML standard that should be used when saving the document to HTML or MHTML"
type: docs
weight: 330
url: /python-net/aspose.words.saving/htmlsaveoptions/html_version/
---

## HtmlSaveOptions.html_version property

Specifies version of HTML standard that should be used when saving the document to HTML or MHTML.
Default value is [HtmlVersion.XHTML](../../htmlversion/#XHTML).



```python
@property
def html_version(self) -> aspose.words.saving.HtmlVersion:
    ...

@html_version.setter
def html_version(self, value: aspose.words.saving.HtmlVersion):
    ...

```

### Examples

Shows how to save a document to a specific version of HTML.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
options = aw.saving.HtmlSaveOptions(aw.SaveFormat.HTML)
options.html_version = html_version
options.pretty_format = True
doc.save(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.HtmlVersions.html', save_options=options)
# Our HTML documents will have minor differences to be compatible with different HTML versions.
out_doc_contents = system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'HtmlSaveOptions.HtmlVersions.html')
switch_condition = html_version
if switch_condition == aw.saving.HtmlVersion.HTML5:
    self.assertTrue('<a id="_Toc76372689"></a>' in out_doc_contents)
    self.assertTrue('<a id="_Toc76372689"></a>' in out_doc_contents)
    self.assertTrue('<table style="padding:0pt; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse">' in out_doc_contents)
elif switch_condition == aw.saving.HtmlVersion.XHTML:
    self.assertTrue('<a name="_Toc76372689"></a>' in out_doc_contents)
    self.assertTrue('<ul type="disc" style="margin:0pt; padding-left:0pt">' in out_doc_contents)
    self.assertTrue('<table cellspacing="0" cellpadding="0" style="-aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse"' in out_doc_contents)
```

Shows how to display a DOCTYPE heading when converting documents to the Xhtml 1.0 transitional standard.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
options = aw.saving.HtmlSaveOptions(aw.SaveFormat.HTML)
options.html_version = aw.saving.HtmlVersion.XHTML
options.export_xhtml_transitional = show_doctype_declaration
options.pretty_format = True
doc.save(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.ExportXhtmlTransitional.html', save_options=options)
# Our document will only contain a DOCTYPE declaration heading if we have set the "ExportXhtmlTransitional" flag to "true".
out_doc_contents = system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'HtmlSaveOptions.ExportXhtmlTransitional.html')
if show_doctype_declaration:
    self.assertTrue('<?xml version="1.0" encoding="utf-8" standalone="no"?>\r\n' + '<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">\r\n' + '<html xmlns="http://www.w3.org/1999/xhtml">' in out_doc_contents)
else:
    self.assertTrue('<html>' in out_doc_contents)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

