---
title: HtmlSaveOptions.export_page_setup property
linktitle: export_page_setup property
articleTitle: export_page_setup property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.export_page_setup property. Specifies whether page setup is exported to HTML, MHTML or EPUB"
type: docs
weight: 220
url: /python-net/aspose.words.saving/htmlsaveoptions/export_page_setup/
---

## HtmlSaveOptions.export_page_setup property

Specifies whether page setup is exported to HTML, MHTML or EPUB.
Default is ``False``.



```python
@property
def export_page_setup(self) -> bool:
    ...

@export_page_setup.setter
def export_page_setup(self, value: bool):
    ...

```

### Remarks

Each [Section](../../../aspose.words/section/) in Aspose.Words document model provides page setup information
via [PageSetup](../../../aspose.words/pagesetup/) class. When you export a document to HTML format you might need to keep this information
for further usage. In particular, page setup might be important for rendering to paged media (printing)
or subsequent conversion to the native Microsoft Word file formats (DOCX, DOC, RTF, WML).

In most cases HTML is intended for viewing in browsers where pagination is not performed. So this feature
is inactive by default.




### Examples

Shows how decide whether to preserve section structure/page setup information when saving to HTML.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('Section 1')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.write('Section 2')
page_setup = doc.sections[0].page_setup
page_setup.top_margin = 36
page_setup.bottom_margin = 36
page_setup.paper_size = aw.PaperSize.A5
# When saving the document to HTML, we can pass a SaveOptions object
# to decide whether to preserve or discard page setup settings.
# If we set the "ExportPageSetup" flag to "true", the output HTML document will contain our page setup configuration.
# If we set the "ExportPageSetup" flag to "false", the save operation will discard our page setup settings
# for the first section, and both sections will look identical.
options = aw.saving.HtmlSaveOptions()
options.export_page_setup = export_page_setup
doc.save(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.ExportPageSetup.html', save_options=options)
out_doc_contents = system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'HtmlSaveOptions.ExportPageSetup.html')
if export_page_setup:
    self.assertTrue('<style type="text/css">' + '@page Section_1 { size:419.55pt 595.3pt; margin:36pt 70.85pt; -aw-footer-distance:35.4pt; -aw-header-distance:35.4pt }' + '@page Section_2 { size:612pt 792pt; margin:70.85pt; -aw-footer-distance:35.4pt; -aw-header-distance:35.4pt }' + 'div.Section_1 { page:Section_1 }div.Section_2 { page:Section_2 }' + '</style>' in out_doc_contents)
    self.assertTrue('<div class="Section_1">' + '<p style="margin-top:0pt; margin-bottom:0pt">' + '<span>Section 1</span>' + '</p>' + '</div>' in out_doc_contents)
else:
    self.assertFalse('style type="text/css">' in out_doc_contents)
    self.assertTrue('<div>' + '<p style="margin-top:0pt; margin-bottom:0pt">' + '<span>Section 1</span>' + '</p>' + '</div>' in out_doc_contents)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

