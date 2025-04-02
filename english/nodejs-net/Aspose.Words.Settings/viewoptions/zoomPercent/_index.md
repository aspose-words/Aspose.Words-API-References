---
title: ViewOptions.zoomPercent property
linktitle: zoomPercent property
articleTitle: zoomPercent property
second_title: Aspose.Words for NodeJs
description: "ViewOptions.zoomPercent property. Gets or sets the percentage (between 10 and 500) at which you want to view your document."
type: docs
weight: 50
url: /nodejs-net/Aspose.Words.Settings/viewoptions/zoomPercent/
---

## ViewOptions.zoomPercent property

Gets or sets the percentage (between 10 and 500) at which you want to view your document.


```js
get zoomPercent(): number
```

### Remarks

If value is 0 then this property uses 100 instead, else if value is less than 10 or greater 
than 500 this property throws.

Although Aspose.Words is able to read and write this option, its usage is application-specific. 
For example MS Word 2013 does not respect the value of this option.




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

* module [Aspose.Words.Settings](../../)
* class [ViewOptions](../)

