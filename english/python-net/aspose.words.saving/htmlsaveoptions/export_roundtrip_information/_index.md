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
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
# When converting a document to .html, some elements such as hidden bookmarks, original shape positions,
# or footnotes will be either removed or converted to plain text and effectively be lost.
# Saving with a HtmlSaveOptions object with ExportRoundtripInformation set to true will preserve these elements.
# When we save the document to HTML, we can pass a SaveOptions object to determine
# how the saving operation will export document elements that HTML does not support or use,
# such as hidden bookmarks and original shape positions.
# If we set the "ExportRoundtripInformation" flag to "true", the save operation will preserve these elements.
# If we set the "ExportRoundTripInformation" flag to "false", the save operation will discard these elements.
# We will want to preserve such elements if we intend to load the saved HTML using Aspose.Words,
# as they could be of use once again.
options = aw.saving.HtmlSaveOptions()
options.export_roundtrip_information = export_roundtrip_information
doc.save(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.RoundTripInformation.html', save_options=options)
out_doc_contents = system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'HtmlSaveOptions.RoundTripInformation.html')
doc = aw.Document(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.RoundTripInformation.html')
if export_roundtrip_information:
    self.assertTrue('<div style="-aw-headerfooter-type:header-primary; clear:both">' in out_doc_contents)
    self.assertTrue('<span style="-aw-import:ignore">&#xa0;</span>' in out_doc_contents)
    self.assertTrue('td colspan="2" style="width:210.6pt; border-style:solid; border-width:0.75pt 6pt 0.75pt 0.75pt; ' + 'padding-right:2.4pt; padding-left:5.03pt; vertical-align:top; -aw-border-bottom:0.5pt single #000000; ' + '-aw-border-left:0.5pt single #000000; -aw-border-right:6pt single #000000; -aw-border-top:0.5pt single #000000">' in out_doc_contents)
    self.assertTrue('<li style="margin-left:30.2pt; padding-left:5.8pt; -aw-font-family:\'Courier New\'; -aw-font-weight:normal; -aw-number-format:\'o\'">' in out_doc_contents)
    self.assertTrue('<img src="HtmlSaveOptions.RoundTripInformation.003.jpeg" width="350" height="180" alt="" ' + 'style="-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline" />' in out_doc_contents)
    self.assertTrue('<span>Page number </span>' + '<span style="-aw-field-start:true"></span>' + '<span style="-aw-field-code:\' PAGE   \\\\* MERGEFORMAT \'"></span>' + '<span style="-aw-field-separator:true"></span>' + '<span>1</span>' + '<span style="-aw-field-end:true"></span>' in out_doc_contents)
    self.assertEqual(1, len(list(filter(lambda f: f.type == aw.fields.FieldType.FIELD_PAGE, doc.range.fields))))
else:
    self.assertTrue('<div style="clear:both">' in out_doc_contents)
    self.assertTrue('<span>&#xa0;</span>' in out_doc_contents)
    self.assertTrue('<td colspan="2" style="width:210.6pt; border-style:solid; border-width:0.75pt 6pt 0.75pt 0.75pt; ' + 'padding-right:2.4pt; padding-left:5.03pt; vertical-align:top">' in out_doc_contents)
    self.assertTrue('<li style="margin-left:30.2pt; padding-left:5.8pt">' in out_doc_contents)
    self.assertTrue('<img src="HtmlSaveOptions.RoundTripInformation.003.jpeg" width="350" height="180" alt="" />' in out_doc_contents)
    self.assertTrue('<span>Page number 1</span>' in out_doc_contents)
    self.assertEqual(0, len(list(filter(lambda f: f.type == aw.fields.FieldType.FIELD_PAGE, doc.range.fields))))
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

