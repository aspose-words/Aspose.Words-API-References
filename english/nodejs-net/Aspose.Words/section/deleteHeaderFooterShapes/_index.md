---
title: Section.deleteHeaderFooterShapes method
linktitle: deleteHeaderFooterShapes method
articleTitle: deleteHeaderFooterShapes method
second_title: Aspose.Words for NodeJs
description: "Section.deleteHeaderFooterShapes method. Deletes all shapes (drawing objects) from the headers and footers of this section."
type: docs
weight: 120
url: /nodejs-net/aspose.words/section/deleteHeaderFooterShapes/
---

## deleteHeaderFooterShapes() {#default}

Deletes all shapes (drawing objects) from the headers and footers of this section.


```js
deleteHeaderFooterShapes()
```

### Examples

Shows how to remove all shapes from all headers footers in a section.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Create a primary header with a shape.
builder.moveToHeaderFooter(aw.HeaderFooterType.HeaderPrimary);
builder.insertShape(aw.Drawing.ShapeType.Rectangle, 100, 100);

// Create a primary footer with an image.
builder.moveToHeaderFooter(aw.HeaderFooterType.FooterPrimary);
builder.insertImage(base.imageDir + "Logo Icon.ico");

expect(doc.firstSection.headersFooters.getByHeaderFooterType(aw.HeaderFooterType.HeaderPrimary).getChildNodes(aw.NodeType.Shape, true).count).toEqual(1);
expect(doc.firstSection.headersFooters.getByHeaderFooterType(aw.HeaderFooterType.FooterPrimary).getChildNodes(aw.NodeType.Shape, true).count).toEqual(1);

// Remove all shapes from the headers and footers in the first section.
doc.firstSection.deleteHeaderFooterShapes();

expect(doc.firstSection.headersFooters.getByHeaderFooterType(aw.HeaderFooterType.HeaderPrimary).getChildNodes(aw.NodeType.Shape, true).count).toEqual(0);
expect(doc.firstSection.headersFooters.getByHeaderFooterType(aw.HeaderFooterType.FooterPrimary).getChildNodes(aw.NodeType.Shape, true).count).toEqual(0);
```

### See Also

* module [Aspose.Words](../../)
* class [Section](../)

