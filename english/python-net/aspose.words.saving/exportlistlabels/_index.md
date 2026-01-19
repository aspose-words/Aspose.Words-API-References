---
title: ExportListLabels enumeration
linktitle: ExportListLabels enumeration
articleTitle: ExportListLabels enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.ExportListLabels enumeration. Specifies how list labels are exported to HTML, MHTML and EPUB."
type: docs
weight: 190
url: /python-net/aspose.words.saving/exportlistlabels/
---

## ExportListLabels enumeration

Specifies how list labels are exported to HTML, MHTML and EPUB.


### Members

| Name | Description |
| --- | --- |
| AUTO | Outputs list labels in auto mode. Uses HTML native elements when possible. |
| AS_INLINE_TEXT | Outputs all list labels as inline text. |
| BY_HTML_TAGS | Outputs all list labels as HTML native elements. |

### Examples

Shows how to configure list exporting to HTML.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
doc_list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
builder.list_format.list = doc_list
builder.writeln('Default numbered list item 1.')
builder.writeln('Default numbered list item 2.')
builder.list_format.list_indent()
builder.writeln('Default numbered list item 3.')
builder.list_format.remove_numbers()
doc_list = doc.lists.add(list_template=aw.lists.ListTemplate.OUTLINE_HEADINGS_LEGAL)
builder.list_format.list = doc_list
builder.writeln('Outline legal heading list item 1.')
builder.writeln('Outline legal heading list item 2.')
builder.list_format.list_indent()
builder.writeln('Outline legal heading list item 3.')
builder.list_format.list_indent()
builder.writeln('Outline legal heading list item 4.')
builder.list_format.list_indent()
builder.writeln('Outline legal heading list item 5.')
builder.list_format.remove_numbers()
# When saving the document to HTML, we can pass a SaveOptions object
# to decide which HTML elements the document will use to represent lists.
# Setting the "ExportListLabels" property to "ExportListLabels.AsInlineText"
# will create lists by formatting spans.
# Setting the "ExportListLabels" property to "ExportListLabels.Auto" will use the <p> tag
# to build lists in cases when using the <ol> and <li> tags may cause loss of formatting.
# Setting the "ExportListLabels" property to "ExportListLabels.ByHtmlTags"
# will use <ol> and <li> tags to build all lists.
options = aw.saving.HtmlSaveOptions()
options.export_list_labels = export_list_labels
doc.save(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.List.html', save_options=options)
out_doc_contents = system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'HtmlSaveOptions.List.html')
switch_condition = export_list_labels
if switch_condition == aw.saving.ExportListLabels.AS_INLINE_TEXT:
    self.assertTrue('<p style="margin-top:0pt; margin-left:72pt; margin-bottom:0pt; text-indent:-18pt; -aw-import:list-item; -aw-list-level-number:1; -aw-list-number-format:\'%1.\'; -aw-list-number-styles:\'lowerLetter\'; -aw-list-number-values:\'1\'; -aw-list-padding-sml:9.67pt">' + '<span style="-aw-import:ignore">' + '<span>a.</span>' + '<span style="width:9.67pt; font:7pt \'Times New Roman\'; display:inline-block; -aw-import:spaces">&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0; </span>' + '</span>' + '<span>Default numbered list item 3.</span>' + '</p>' in out_doc_contents)
    self.assertTrue('<p style="margin-top:0pt; margin-left:43.2pt; margin-bottom:0pt; text-indent:-43.2pt; -aw-import:list-item; -aw-list-level-number:3; -aw-list-number-format:\'%0.%1.%2.%3\'; -aw-list-number-styles:\'decimal decimal decimal decimal\'; -aw-list-number-values:\'2 1 1 1\'; -aw-list-padding-sml:10.2pt">' + '<span style="-aw-import:ignore">' + '<span>2.1.1.1</span>' + '<span style="width:10.2pt; font:7pt \'Times New Roman\'; display:inline-block; -aw-import:spaces">&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0; </span>' + '</span>' + '<span>Outline legal heading list item 5.</span>' + '</p>' in out_doc_contents)
elif switch_condition == aw.saving.ExportListLabels.AUTO:
    self.assertTrue('<ol type="a" style="margin-right:0pt; margin-left:0pt; padding-left:0pt">' + '<li style="margin-left:31.33pt; padding-left:4.67pt">' + '<span>Default numbered list item 3.</span>' + '</li>' + '</ol>' in out_doc_contents)
elif switch_condition == aw.saving.ExportListLabels.BY_HTML_TAGS:
    self.assertTrue('<ol type="a" style="margin-right:0pt; margin-left:0pt; padding-left:0pt">' + '<li style="margin-left:31.33pt; padding-left:4.67pt">' + '<span>Default numbered list item 3.</span>' + '</li>' + '</ol>' in out_doc_contents)
```

### See Also

* module [aspose.words.saving](../)
* property [HtmlSaveOptions.export_list_labels](../htmlsaveoptions/export_list_labels/)

