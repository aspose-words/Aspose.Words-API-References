---
title: ZoomType enumeration
linktitle: ZoomType enumeration
articleTitle: ZoomType enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Settings.ZoomType enumeration. Possible values for how large or small the document appears on the screen in Microsoft Word."
type: docs
weight: 220
url: /nodejs-net/aspose.words.settings/zoomtype/
---

## ZoomType enumeration

Possible values for how large or small the document appears on the screen in Microsoft Word.


### Members

| Name | Description |
| --- | --- |
| Custom | Zoom percentage is set explicitly. It is not recalculated automatically when control size changes. |
| None | Indicates to use the explicit zoom percentage. Same as [ZoomType.Custom](./#Custom). |
| FullPage | Zoom percentage is automatically recalculated to fit one full page. |
| PageWidth | Zoom percentage is automatically recalculated to fit page width. |
| TextFit | Zoom percentage is automatically recalculated to fit text. |

### Examples

Shows how to set a custom zoom factor, which older versions of Microsoft Word will apply to a document upon loading.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
builder.writeln("Hello world!");

doc.viewOptions.viewType = aw.Settings.ViewType.PageLayout;
doc.viewOptions.zoomPercent = 50;

expect(doc.viewOptions.zoomType).toEqual(aw.Settings.ZoomType.Custom);
expect(doc.viewOptions.zoomType).toEqual(aw.Settings.ZoomType.None);

doc.save(base.artifactsDir + "ViewOptions.SetZoomPercentage.doc");
```

### See Also

* module [Aspose.Words.Settings](../)
* class [ViewOptions](../viewoptions/)
* property [ViewOptions.zoomType](../viewoptions/zoomType/)

