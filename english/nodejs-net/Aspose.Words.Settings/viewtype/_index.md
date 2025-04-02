---
title: ViewType enumeration
linktitle: ViewType enumeration
articleTitle: ViewType enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Settings.ViewType enumeration. Possible values for the view mode in Microsoft Word."
type: docs
weight: 200
url: /nodejs-net/Aspose.Words.Settings/viewtype/
---

## ViewType enumeration

Possible values for the view mode in Microsoft Word.


### Members

| Name | Description |
| --- | --- |
| None | The document shall be rendered in the default view of the application. |
| Reading | The document shall be rendered in the default view of the application. |
| PageLayout | The document shall be opened in a view that displays the document as it will print. |
| Outline | The document shall be rendered in a view optimized for outlining or creating long documents. |
| Normal | The document shall be rendered in a view optimized for outlining or creating long documents. |
| Web | The document shall be rendered in a view mimicking the way this document would be displayed  in a web page. |

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
* property [ViewOptions.viewType](../viewoptions/viewType/)

