---
title: export_page_setup property
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies whether page setup is exported to HTML, MHTML or EPUB"
type: docs
weight: 230
url: /python-net/aspose.words.saving/htmlsaveoptions/export_page_setup/
---

## HtmlSaveOptions.export_page_setup property

Specifies whether page setup is exported to HTML, MHTML or EPUB.
Default is ``false``.


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
builder = aw.DocumentBuilder(doc)

builder.write("Section 1")
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.write("Section 2")

page_setup = doc.sections[0].page_setup
page_setup.top_margin = 36.0
page_setup.bottom_margin = 36.0
page_setup.paper_size = aw.PaperSize.A5

# When saving the document to HTML, we can pass a SaveOptions object
# to decide whether to preserve or discard page setup settings.
# If we set the "export_page_setup" flag to "True", the output HTML document will contain our page setup configuration.
# If we set the "export_page_setup" flag to "False", the save operation will discard our page setup settings
# for the first section, and both sections will look identical.
options = aw.saving.HtmlSaveOptions()
options.export_page_setup = export_page_setup

doc.save(ARTIFACTS_DIR + "HtmlSaveOptions.export_page_setup.html", options)

with open(ARTIFACTS_DIR + "HtmlSaveOptions.export_page_setup.html", "rt", encoding="utf-8") as file:
    out_doc_contents = file.read()

if export_page_setup:
    self.assertIn(
        "<style type=\"text/css\">" +
            "@page Section1 { size:419.55pt 595.3pt; margin:36pt 70.85pt }" +
            "@page Section2 { size:612pt 792pt; margin:70.85pt }" +
            "div.Section1 { page:Section1 }div.Section2 { page:Section2 }" +
        "</style>", out_doc_contents)

    self.assertIn(
        "<div class=\"Section1\">" +
            "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                "<span>Section 1</span>" +
            "</p>" +
        "</div>", out_doc_contents)
else:
    self.assertNotIn("style type=\"text/css\">", out_doc_contents)

    self.assertIn(
        "<div>" +
            "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                "<span>Section 1</span>" +
            "</p>" +
        "</div>", out_doc_contents)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

