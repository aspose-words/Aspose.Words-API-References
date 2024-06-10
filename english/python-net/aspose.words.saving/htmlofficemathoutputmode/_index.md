---
title: HtmlOfficeMathOutputMode enumeration
linktitle: HtmlOfficeMathOutputMode enumeration
articleTitle: HtmlOfficeMathOutputMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.HtmlOfficeMathOutputMode enumeration. Specifies how Aspose.Words exports OfficeMath to HTML, MHTML and EPUB."
type: docs
weight: 260
url: /python-net/aspose.words.saving/htmlofficemathoutputmode/
---

## HtmlOfficeMathOutputMode enumeration

Specifies how Aspose.Words exports OfficeMath to HTML, MHTML and EPUB.


### Members

| Name | Description |
| --- | --- |
| IMAGE | OfficeMath is converted to HTML as image specified by \<img\> tag. |
| MATH_ML | OfficeMath is converted to HTML using MathML. |
| TEXT | OfficeMath is converted to HTML as sequence of runs specified by \<span\> tags. |

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
    self.assertRegex(out_doc_contents, '<p style="margin-top:0pt; margin-bottom:10pt">' + '<img src="HtmlSaveOptions.office_math_output_mode.001.png" width="160" height="19" alt="" style="vertical-align:middle; ' + '-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline" />' + '</p>')
elif html_office_math_output_mode == aw.saving.HtmlOfficeMathOutputMode.MATH_ML:
    self.assertRegex(out_doc_contents, '<p style="margin-top:0pt; margin-bottom:10pt; text-align:center">' + '<math xmlns="http://www.w3.org/1998/Math/MathML">' + '<mi>i</mi>' + '<mo>[+]</mo>' + '<mi>b</mi>' + '<mo>-</mo>' + '<mi>c</mi>' + '<mo>≥</mo>' + '.*' + '</math>' + '</p>')
elif html_office_math_output_mode == aw.saving.HtmlOfficeMathOutputMode.TEXT:
    self.assertRegex(out_doc_contents, '<p style="margin-top:0pt; margin-bottom:10pt; text-align:center">' + '<span style="font-family:\\\'Cambria Math\\\'">i[+]b-c≥iM[+]bM-cM </span>' + '</p>')
```

### See Also

* module [aspose.words.saving](../)

