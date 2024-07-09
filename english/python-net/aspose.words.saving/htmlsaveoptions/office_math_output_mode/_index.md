---
title: HtmlSaveOptions.office_math_output_mode property
linktitle: office_math_output_mode property
articleTitle: office_math_output_mode property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.office_math_output_mode property. Controls how OfficeMath objects are exported to HTML, MHTML or EPUB"
type: docs
weight: 400
url: /python-net/aspose.words.saving/htmlsaveoptions/office_math_output_mode/
---

## HtmlSaveOptions.office_math_output_mode property

Controls how OfficeMath objects are exported to HTML, MHTML or EPUB.
Default value is [HtmlOfficeMathOutputMode.IMAGE](../../htmlofficemathoutputmode/#IMAGE).



```python
@property
def office_math_output_mode(self) -> aspose.words.saving.HtmlOfficeMathOutputMode:
    ...

@office_math_output_mode.setter
def office_math_output_mode(self, value: aspose.words.saving.HtmlOfficeMathOutputMode):
    ...

```

### Examples

Shows how to specify how to export Microsoft OfficeMath objects to HTML.

```python
doc = aw.Document(MY_DIR + 'Office math.docx')
# When we save the document to HTML, we can pass a SaveOptions object
# to determine how the saving operation handles OfficeMath objects.
# Setting the "office_math_output_mode" property to "HtmlOfficeMathOutputMode.IMAGE"
# will render each OfficeMath object into an image.
# Setting the "office_math_output_mode" property to "HtmlOfficeMathOutputMode.MATH_ML"
# will convert each OfficeMath object into MathML.
# Setting the "office_math_output_mode" property to "HtmlOfficeMathOutputMode.TEXT"
# will represent each OfficeMath formula using plain HTML text.
options = aw.saving.HtmlSaveOptions()
options.office_math_output_mode = html_office_math_output_mode
doc.save(ARTIFACTS_DIR + 'HtmlSaveOptions.office_math_output_mode.html', options)
with open(ARTIFACTS_DIR + 'HtmlSaveOptions.office_math_output_mode.html', 'rt', encoding='utf-8') as file:
    out_doc_contents = file.read()
if html_office_math_output_mode == aw.saving.HtmlOfficeMathOutputMode.IMAGE:
    self.assertRegex(out_doc_contents, '<p style="margin-top:0pt; margin-bottom:10pt">' + '<img src="HtmlSaveOptions.office_math_output_mode.001.png" width="163" height="19" alt="" style="vertical-align:middle; ' + '-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline" />' + '</p>')
elif html_office_math_output_mode == aw.saving.HtmlOfficeMathOutputMode.MATH_ML:
    self.assertRegex(out_doc_contents, '<p style="margin-top:0pt; margin-bottom:10pt; text-align:center">' + '<math xmlns="http://www.w3.org/1998/Math/MathML">' + '<mi>i</mi>' + '<mo>[+]</mo>' + '<mi>b</mi>' + '<mo>-</mo>' + '<mi>c</mi>' + '<mo>≥</mo>' + '.*' + '</math>' + '</p>')
elif html_office_math_output_mode == aw.saving.HtmlOfficeMathOutputMode.TEXT:
    self.assertRegex(out_doc_contents, '<p style="margin-top:0pt; margin-bottom:10pt; text-align:center">' + '<span style="font-family:\\\'Cambria Math\\\'">i[+]b-c≥iM[+]bM-cM </span>' + '</p>')
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

