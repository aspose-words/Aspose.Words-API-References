---
title: HtmlSaveOptions.export_list_labels property
linktitle: export_list_labels property
articleTitle: export_list_labels property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.export_list_labels property. Controls how list labels are output to HTML, MHTML or EPUB"
type: docs
weight: 190
url: /python-net/aspose.words.saving/htmlsaveoptions/export_list_labels/
---

## HtmlSaveOptions.export_list_labels property

Controls how list labels are output to HTML, MHTML or EPUB. 
Default value is [ExportListLabels.AUTO](../../exportlistlabels/#AUTO).



```python
@property
def export_list_labels(self) -> aspose.words.saving.ExportListLabels:
    ...

@export_list_labels.setter
def export_list_labels(self, value: aspose.words.saving.ExportListLabels):
    ...

```

### Examples

Shows how to configure list exporting to HTML.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
list = doc.lists.add(aw.lists.ListTemplate.NUMBER_DEFAULT)
builder.list_format.list = list
builder.writeln('Default numbered list item 1.')
builder.writeln('Default numbered list item 2.')
builder.list_format.list_indent()
builder.writeln('Default numbered list item 3.')
builder.list_format.remove_numbers()
list = doc.lists.add(aw.lists.ListTemplate.OUTLINE_HEADINGS_LEGAL)
builder.list_format.list = list
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
# Setting the "export_list_labels" property to "ExportListLabels.AS_INLINE_TEXT"
# will create lists by formatting spans.
# Setting the "export_list_labels" property to "ExportListLabels.AUTO" will use the <p> tag
# to build lists in cases when using the <ol> and <li> tags may cause loss of formatting.
# Setting the "export_list_labels" property to "ExportListLabels.BY_HTML_TAGS"
# will use <ol> and <li> tags to build all lists.
options = aw.saving.HtmlSaveOptions()
options.export_list_labels = export_list_labels
doc.save(ARTIFACTS_DIR + 'HtmlSaveOptions.list.html', options)
with open(ARTIFACTS_DIR + 'HtmlSaveOptions.list.html', 'rt', encoding='utf-8') as file:
    out_doc_contents = file.read()
if export_list_labels == aw.saving.ExportListLabels.AS_INLINE_TEXT:
    self.assertIn('<p style="margin-top:0pt; margin-left:72pt; margin-bottom:0pt; text-indent:-18pt; -aw-import:list-item; -aw-list-level-number:1; -aw-list-number-format:\'%1.\'; -aw-list-number-styles:\'lowerLetter\'; -aw-list-number-values:\'1\'; -aw-list-padding-sml:9.67pt">' + '<span style="-aw-import:ignore">' + '<span>a.</span>' + '<span style="width:9.67pt; font:7pt \'Times New Roman\'; display:inline-block; -aw-import:spaces">&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0; </span>' + '</span>' + '<span>Default numbered list item 3.</span>' + '</p>', out_doc_contents)
    self.assertIn('<p style="margin-top:0pt; margin-left:43.2pt; margin-bottom:0pt; text-indent:-43.2pt; -aw-import:list-item; -aw-list-level-number:3; -aw-list-number-format:\'%0.%1.%2.%3\'; -aw-list-number-styles:\'decimal decimal decimal decimal\'; -aw-list-number-values:\'2 1 1 1\'; -aw-list-padding-sml:10.2pt">' + '<span style="-aw-import:ignore">' + '<span>2.1.1.1</span>' + '<span style="width:10.2pt; font:7pt \'Times New Roman\'; display:inline-block; -aw-import:spaces">&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0; </span>' + '</span>' + '<span>Outline legal heading list item 5.</span>' + '</p>', out_doc_contents)
elif export_list_labels == aw.saving.ExportListLabels.AUTO:
    self.assertIn('<ol type="a" style="margin-right:0pt; margin-left:0pt; padding-left:0pt">' + '<li style="margin-left:31.33pt; padding-left:4.67pt">' + '<span>Default numbered list item 3.</span>' + '</li>' + '</ol>', out_doc_contents)
elif export_list_labels == aw.saving.ExportListLabels.BY_HTML_TAGS:
    self.assertIn('<ol type="a" style="margin-right:0pt; margin-left:0pt; padding-left:0pt">' + '<li style="margin-left:31.33pt; padding-left:4.67pt">' + '<span>Default numbered list item 3.</span>' + '</li>' + '</ol>', out_doc_contents)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

