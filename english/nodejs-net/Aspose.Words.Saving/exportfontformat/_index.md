---
title: ExportFontFormat enumeration
linktitle: ExportFontFormat enumeration
articleTitle: ExportFontFormat enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Saving.ExportFontFormat enumeration. Indicates the format that is used to export fonts while rendering to HTML fixed format."
type: docs
weight: 160
url: /nodejs-net/aspose.words.saving/exportfontformat/
---

## ExportFontFormat enumeration

Indicates the format that is used to export fonts while rendering to HTML fixed format.


### Members

| Name | Description |
| --- | --- |
| Woff | WOFF (Web Open Font Format). |
| Ttf | TTF (TrueType Font format). |

### Examples

Shows how use fonts only from the target machine when saving a document to HTML.

```js
let doc = new aw.Document(base.myDir + "Bullet points with alternative font.docx");

let saveOptions = new aw.Saving.HtmlFixedSaveOptions();
saveOptions.exportEmbeddedCss = true;
saveOptions.useTargetMachineFonts = useTargetMachineFonts;
saveOptions.fontFormat = aw.Saving.ExportFontFormat.Ttf;
saveOptions.exportEmbeddedFonts = false;

doc.save(base.artifactsDir + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

let outDocContents = fs.readFileSync(base.artifactsDir + "HtmlFixedSaveOptions.UsingMachineFonts.html").toString();

if (useTargetMachineFonts)
  expect(outDocContents.includes("@font-face")).toBeFalsy();
else
  expect(outDocContents.includes("@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local('☺'), " +
"url('HtmlFixedSaveOptions.UsingMachineFonts/font001.ttf') format('truetype'); }")).toBeTruthy();
```

### See Also

* module [Aspose.Words.Saving](../)
* property [HtmlFixedSaveOptions.fontFormat](../htmlfixedsaveoptions/fontFormat/)

