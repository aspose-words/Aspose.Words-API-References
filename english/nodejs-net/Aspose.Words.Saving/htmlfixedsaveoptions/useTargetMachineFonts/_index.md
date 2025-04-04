---
title: HtmlFixedSaveOptions.useTargetMachineFonts property
linktitle: useTargetMachineFonts property
articleTitle: useTargetMachineFonts property
second_title: Aspose.Words for Node.js
description: "HtmlFixedSaveOptions.useTargetMachineFonts property. Flag indicates whether fonts from target machine must be used to display the document"
type: docs
weight: 210
url: /nodejs-net/aspose.words.saving/htmlfixedsaveoptions/useTargetMachineFonts/
---

## HtmlFixedSaveOptions.useTargetMachineFonts property

Flag indicates whether fonts from target machine must be used to display the document.
If this flag is set to ``true``, [HtmlFixedSaveOptions.fontFormat](../fontFormat/) and [HtmlFixedSaveOptions.exportEmbeddedFonts](../exportEmbeddedFonts/) properties do not have effect,
also [HtmlFixedSaveOptions.resourceSavingCallback](../resourceSavingCallback/) is not fired for fonts.
Default is ``false``.



```js
get useTargetMachineFonts(): boolean
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

