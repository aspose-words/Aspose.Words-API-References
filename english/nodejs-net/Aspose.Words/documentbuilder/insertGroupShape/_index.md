---
title: DocumentBuilder.insertGroupShape method
linktitle: insertGroupShape method
articleTitle: insertGroupShape method
second_title: Aspose.Words for Node.js
description: "Aspose.Words.DocumentBuilder.insertGroupShape method"
type: docs
weight: 360
url: /nodejs-net/aspose.words/documentbuilder/insertGroupShape/
---

## insertGroupShape(shapes) {#shapebase[]}

Groups the shapes passed as a parameter into a new GroupShape node which is inserted into the current position.


```js
insertGroupShape(shapes: Aspose.Words.Drawing.ShapeBase[])
```

| Parameter | Type | Description |
| --- | --- | --- |
| shapes | [ShapeBase](../../../aspose.words.drawing/shapebase/)[] | The list of shapes to be grouped. |

### Remarks

The position and dimension of the new GroupShape will be calculated automatically.

VML and DML shapes cannot be grouped together.




## insertGroupShape(left, top, width, height, shapes) {#number_number_number_number_shapebase[]}

Groups the shapes passed as a parameter into a new GroupShape node of the specified size which is inserted into the specified position.


```js
insertGroupShape(left: number, top: number, width: number, height: number, shapes: Aspose.Words.Drawing.ShapeBase[])
```

| Parameter | Type | Description |
| --- | --- | --- |
| left | number | Distance in points from the origin to the left side of the group shape. |
| top | number | Distance in points from the origin to the top side of the group shape. |
| width | number | The width of the group shape in points. A negative value is not allowed. |
| height | number | The height of the group shape in points. A negative value is not allowed. |
| shapes | [ShapeBase](../../../aspose.words.drawing/shapebase/)[] | The list of shapes to be grouped. |

### Remarks

VML and DML shapes cannot be grouped together.


## See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)

