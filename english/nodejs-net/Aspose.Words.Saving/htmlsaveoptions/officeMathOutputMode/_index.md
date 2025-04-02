---
title: HtmlSaveOptions.officeMathOutputMode property
linktitle: officeMathOutputMode property
articleTitle: officeMathOutputMode property
second_title: Aspose.Words for NodeJs
description: "HtmlSaveOptions.officeMathOutputMode property. Controls how OfficeMath objects are exported to HTML, MHTML or EPUB"
type: docs
weight: 400
url: /nodejs-net/Aspose.Words.Saving/htmlsaveoptions/officeMathOutputMode/
---

## HtmlSaveOptions.officeMathOutputMode property

Controls how OfficeMath objects are exported to HTML, MHTML or EPUB.
Default value is [HtmlOfficeMathOutputMode.Image](../../htmlofficemathoutputmode/#Image).



```js
get officeMathOutputMode(): Aspose.Words.Saving.HtmlOfficeMathOutputMode
```

### Examples

Shows how to specify how to export Microsoft OfficeMath objects to HTML.

```js
let doc = new aw.Document(base.myDir + "Office math.docx");

// When we save the document to HTML, we can pass a SaveOptions object
// to determine how the saving operation handles OfficeMath objects.
// Setting the "OfficeMathOutputMode" property to "HtmlOfficeMathOutputMode.Image"
// will render each OfficeMath object into an image.
// Setting the "OfficeMathOutputMode" property to "HtmlOfficeMathOutputMode.MathML"
// will convert each OfficeMath object into MathML.
// Setting the "OfficeMathOutputMode" property to "HtmlOfficeMathOutputMode.Text"
// will represent each OfficeMath formula using plain HTML text.
let options = new aw.Saving.HtmlSaveOptions();
options.officeMathOutputMode = htmlOfficeMathOutputMode;

doc.save(base.artifactsDir + "HtmlSaveOptions.officeMathOutputMode.html", options);
let outDocContents = fs.readFileSync(base.artifactsDir + "HtmlSaveOptions.officeMathOutputMode.html").toString();

switch (htmlOfficeMathOutputMode)
{
  case aw.Saving.HtmlOfficeMathOutputMode.Image:
    expect(outDocContents.search('<p style="margin-top:0pt; margin-bottom:10pt">' + 
       '<img src="HtmlSaveOptions.officeMathOutputMode.001.png" width="163" height="19" alt="" style="vertical-align:middle; ' +
       '-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline" />' +
       '</p>')).not.toEqual(-1);
    break;
  case aw.Saving.HtmlOfficeMathOutputMode.MathML:
    expect(outDocContents.search(
      '<p style="margin-top:0pt; margin-bottom:10pt; text-align:center">' +
        '<math xmlns="http://www.w3.org/1998/Math/MathML">' +
          '<mi>i</mi>' +
          '<mo>[+]</mo>' +
          '<mi>b</mi>' +
          '<mo>-</mo>' +
          '<mi>c</mi>' +
          '<mo>≥</mo>' +
          '.*' +
        '</math>' +
      '</p>')).not.toEqual(-1);
    break;
  case aw.Saving.HtmlOfficeMathOutputMode.Text:
    expect(outDocContents.search('<p style="margin-top:0pt; margin-bottom:10pt; text-align:center">' +
       `<span style="font-family:'Cambria Math'">i[+]b-c≥iM[+]bM-cM </span>` +
       '</p>')).not.toEqual(-1);
    break;
}
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [HtmlSaveOptions](../)

