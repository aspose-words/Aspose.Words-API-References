---
title: HtmlFixedSaveOptions.fontFormat property
linktitle: fontFormat property
articleTitle: fontFormat property
second_title: Aspose.Words for NodeJs
description: "HtmlFixedSaveOptions.fontFormat property. Gets or sets [ExportFontFormat](../../exportfontformat/) used for font exporting"
type: docs
weight: 90
url: /nodejs-net/aspose.words.saving/htmlfixedsaveoptions/fontFormat/
---

## HtmlFixedSaveOptions.fontFormat property

Gets or sets [ExportFontFormat](../../exportfontformat/) used for font exporting.
Default value is [ExportFontFormat.Woff](../../exportfontformat/#Woff).



```js
get fontFormat(): Aspose.Words.Saving.ExportFontFormat
```

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

* module [Aspose.Words.Saving](../../)
* class [HtmlFixedSaveOptions](../)

