---
title: HtmlSaveOptions.export_roundtrip_information property
linktitle: export_roundtrip_information property
articleTitle: export_roundtrip_information property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.export_roundtrip_information property. Specifies whether to write the roundtrip information when saving to HTML, MHTML or EPUB"
type: docs
weight: 240
url: /python-net/aspose.words.saving/htmlsaveoptions/export_roundtrip_information/
---

## HtmlSaveOptions.export_roundtrip_information property

Specifies whether to write the roundtrip information when saving to HTML, MHTML or EPUB.
Default value is ``True`` for HTML and ``False`` for MHTML and EPUB.



```python
@property
def export_roundtrip_information(self) -> bool:
    ...

@export_roundtrip_information.setter
def export_roundtrip_information(self, value: bool):
    ...

```

### Remarks

Saving of the roundtrip information allows to restore document properties such as tab stops,
comments, headers and footers during the HTML documents loading back into a [Document](../../../aspose.words/document/) object.

When ``True``, the roundtrip information is exported as -aw-\* CSS properties
of the corresponding HTML elements.

When ``False``, causes no roundtrip information to be output into produced files.




### Examples

Shows how to preserve hidden elements when converting to .html.

```python
doc = aw.Document(MY_DIR + 'Rendering.docx')
# When converting a document to .html, some elements such as hidden bookmarks, original shape positions,
# or footnotes will be either removed or converted to plain text and effectively be lost.
# Saving with a HtmlSaveOptions object with "export_roundtrip_information" set to True will preserve these elements.
# When we save the document to HTML, we can pass a SaveOptions object to determine
# how the saving operation will export document elements that HTML does not support or use,
# such as hidden bookmarks and original shape positions.
# If we set the "export_roundtrip_information" flag to "True", the save operation will preserve these elements.
# If we set the "export_roundtrip_information" flag to "False", the save operation will discard these elements.
# We will want to preserve such elements if we intend to load the saved HTML using Aspose.Words,
# as they could be of use once again.
options = aw.saving.HtmlSaveOptions()
options.export_roundtrip_information = export_roundtrip_information
doc.save(ARTIFACTS_DIR + 'HtmlSaveOptions.round_trip_information.html', options)
with open(ARTIFACTS_DIR + 'HtmlSaveOptions.round_trip_information.html', 'rt', encoding='utf-8') as file:
    out_doc_contents = file.read()
doc = aw.Document(ARTIFACTS_DIR + 'HtmlSaveOptions.round_trip_information.html')
if export_roundtrip_information:
    self.assertIn('<div style="-aw-headerfooter-type:header-primary; clear:both">', out_doc_contents)
    self.assertIn('<span style="-aw-import:ignore">&#xa0;</span>', out_doc_contents)
    self.assertIn('td colspan="2" style="width:210.6pt; border-style:solid; border-width:0.75pt 6pt 0.75pt 0.75pt; ' + 'padding-right:2.4pt; padding-left:5.03pt; vertical-align:top; ' + '-aw-border-bottom:0.5pt single; -aw-border-left:0.5pt single; -aw-border-top:0.5pt single">', out_doc_contents)
    self.assertIn('<li style="margin-left:30.2pt; padding-left:5.8pt; -aw-font-family:\'Courier New\'; -aw-font-weight:normal; -aw-number-format:\'o\'">', out_doc_contents)
    self.assertIn('<img src="HtmlSaveOptions.round_trip_information.003.jpeg" width="350" height="180" alt="" ' + 'style="-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline" />', out_doc_contents)
    self.assertIn('<span>Page number </span>' + '<span style="-aw-field-start:true"></span>' + '<span style="-aw-field-code:\' PAGE   \\\\* MERGEFORMAT \'"></span>' + '<span style="-aw-field-separator:true"></span>' + '<span>1</span>' + '<span style="-aw-field-end:true"></span>', out_doc_contents)
    self.assertEqual(1, len([f for f in doc.range.fields if f.type == aw.fields.FieldType.FIELD_PAGE]))
else:
    self.assertIn('<div style="clear:both">', out_doc_contents)
    self.assertIn('<span>&#xa0;</span>', out_doc_contents)
    self.assertIn('<td colspan="2" style="width:210.6pt; border-style:solid; border-width:0.75pt 6pt 0.75pt 0.75pt; ' + 'padding-right:2.4pt; padding-left:5.03pt; vertical-align:top">', out_doc_contents)
    self.assertIn('<li style="margin-left:30.2pt; padding-left:5.8pt">', out_doc_contents)
    self.assertIn('<img src="HtmlSaveOptions.round_trip_information.003.jpeg" width="350" height="180" alt="" />', out_doc_contents)
    self.assertIn('<span>Page number 1</span>', out_doc_contents)
    self.assertEqual(0, len([f for f in doc.range.fields if f.type == aw.fields.FieldType.FIELD_PAGE]))
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

