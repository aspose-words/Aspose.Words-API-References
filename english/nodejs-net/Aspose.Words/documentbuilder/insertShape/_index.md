---
title: DocumentBuilder.insertShape method
linktitle: insertShape method
articleTitle: insertShape method
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.DocumentBuilder.insertShape method"
type: docs
weight: 460
url: /nodejs-net/aspose.words/documentbuilder/insertShape/
---

## insertShape(shapeType, width, height) {#shapetype_number_number}

Inserts inline shape with specified type and size.


```js
insertShape(shapeType: Aspose.Words.Drawing.ShapeTypewidth: numberheight: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| shapeType | [ShapeType](../../../aspose.words.drawing/shapetype/) | The shape type to insert into the document. |
| width | number | The width of the shape in points. |
| height | number | The height of the shape in points. |

### Returns

The shape node that was inserted.


## insertShape(shapeType, horzPos, left, vertPos, top, width, height, wrapType) {#shapetype_relativehorizontalposition_number_relativeverticalposition_number_number_number_wraptype}

Inserts free-floating shape with specified position, size and text wrap type.


```js
insertShape(shapeType: Aspose.Words.Drawing.ShapeTypehorzPos: Aspose.Words.Drawing.RelativeHorizontalPositionleft: numbervertPos: Aspose.Words.Drawing.RelativeVerticalPositiontop: numberwidth: numberheight: numberwrapType: Aspose.Words.Drawing.WrapType)
```

| Parameter | Type | Description |
| --- | --- | --- |
| shapeType | [ShapeType](../../../aspose.words.drawing/shapetype/) | The shape type to insert into the document |
| horzPos | [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/) | Specifies where the horizontal distance to the shape is measured from. |
| left | number | Distance in points from the origin to the left side of the shape. |
| vertPos | [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/) | Specifies where the vertical distance to the shape is measured from. |
| top | number | Distance in points from the origin to the top side of the shape. |
| width | number | The width of the shape in points. |
| height | number | The height of the shape in points. |
| wrapType | [WrapType](../../../aspose.words.drawing/wraptype/) | Specifies how to wrap text around the shape. |

### Returns

The shape node that was inserted.


## See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)

