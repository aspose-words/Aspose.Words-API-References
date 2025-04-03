---
title: ShapeBase.zorder property
linktitle: zorder property
articleTitle: zorder property
second_title: Aspose.Words for NodeJs
description: "ShapeBase.zorder property. Determines the display order of overlapping shapes."
type: docs
weight: 590
url: /nodejs-net/aspose.words.drawing/shapebase/zorder/
---

## ShapeBase.zorder property

Determines the display order of overlapping shapes.


```js
get zorder(): number
```

### Remarks

Has effect only for top level shapes.

The default value is 0.

The number represents the stacking precedence. A shape with a higher number will be displayed
as if it were overlapping (in "front" of) a shape with a lower number.

The order of overlapping shapes is independent for shapes in the header and in the main
text of the document.

The display order of child shapes in a group shape is determined by their order
inside the group shape.




### See Also

* module [Aspose.Words.Drawing](../../)
* class [ShapeBase](../)
* property [ShapeBase.behindText](../behindText/)

