---
title: NodeRendererBase.getOpaqueBoundsInPixels2 method
linktitle: getOpaqueBoundsInPixels2 method
articleTitle: getOpaqueBoundsInPixels2 method
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Rendering.NodeRendererBase.getOpaqueBoundsInPixels2 method"
type: docs
weight: 50
url: /nodejs-net/aspose.words.rendering/noderendererbase/getOpaqueBoundsInPixels2/
---

## getOpaqueBoundsInPixels2(scale, dpi) {#number_number}

Calculates the opaque bounds of the shape in pixels for a specified zoom factor and resolution.


```js
getOpaqueBoundsInPixels2(scale: number, dpi: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| scale | number | The zoom factor (1.0 is 100%). |
| dpi | number | The resolution to convert from points to pixels (dots per inch). |

### Remarks

This method converts Aspose.Words.Rendering.NodeRendererBase.OpaqueBoundsInPoints into rectangle in pixels and it is useful
when you want to create a bitmap for rendering the shape with only opaque part of the shape.




### Returns

The opaque rectangle of the shape in pixels.


## getOpaqueBoundsInPixels2(scale, horizontalDpi, verticalDpi) {#number_number_number}

Calculates the opaque bounds of the shape in pixels for a specified zoom factor and resolution.


```js
getOpaqueBoundsInPixels2(scale: number, horizontalDpi: number, verticalDpi: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| scale | number | The zoom factor (1.0 is 100%). |
| horizontalDpi | number | The horizontal resolution to convert from points to pixels (dots per inch). |
| verticalDpi | number | The vertical resolution to convert from points to pixels (dots per inch). |

### Remarks

This method converts Aspose.Words.Rendering.NodeRendererBase.OpaqueBoundsInPoints into rectangle in pixels and it is useful
when you want to create a bitmap for rendering the shape with only opaque part of the shape.




### Returns

The opaque rectangle of the shape in pixels.


## See Also

* module [Aspose.Words.Rendering](../../)
* class [NodeRendererBase](../)

