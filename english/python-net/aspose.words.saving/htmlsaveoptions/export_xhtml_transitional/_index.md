---
title: HtmlSaveOptions.export_xhtml_transitional property
linktitle: export_xhtml_transitional property
articleTitle: export_xhtml_transitional property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.export_xhtml_transitional property. Specifies whether to write the DOCTYPE declaration when saving to HTML or MHTML"
type: docs
weight: 280
url: /python-net/aspose.words.saving/htmlsaveoptions/export_xhtml_transitional/
---

## HtmlSaveOptions.export_xhtml_transitional property

Specifies whether to write the DOCTYPE declaration when saving to HTML or MHTML.
When ``True``, writes a DOCTYPE declaration in the document prior to the root element. 
Default value is ``False``.
When saving to EPUB or HTML5 ([HtmlVersion.HTML5](../../htmlversion/#HTML5)) the DOCTYPE
declaration is always written.



```python
@property
def export_xhtml_transitional(self) -> bool:
    ...

@export_xhtml_transitional.setter
def export_xhtml_transitional(self, value: bool):
    ...

```

### Remarks

Aspose.Words always writes well formed HTML regardless of this setting.

When ``True``, the beginning of the HTML output document will look like this:

```

<?xml version="1.0" encoding="utf-8" standalone="no" ?>
<!DOCTYPE html 
      PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">

```
Aspose.Words aims to output XHTML according to the XHTML 1.0 Transitional specification, 
but the output will not always validate against the DTD. Some structures inside a Microsoft Word 
document are hard or impossible to map to a document that will validate against the XHTML schema. 
For example, XHTML does not allow nested lists (UL cannot be nested inside another UL element), 
but in Microsoft Word document multilevel lists occur quite often.




### Examples

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

