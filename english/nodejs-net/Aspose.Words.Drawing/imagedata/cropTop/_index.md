---
title: ImageData.cropTop property
linktitle: cropTop property
articleTitle: cropTop property
second_title: Aspose.Words for NodeJs
description: "ImageData.cropTop property. Defines the fraction of picture removal from the top side."
type: docs
weight: 90
url: /nodejs-net/aspose.words.drawing/imagedata/cropTop/
---

## ImageData.cropTop property

Defines the fraction of picture removal from the top side.


```js
get cropTop(): number
```

### Remarks

The amount of cropping can range from -1.0 to 1.0. The default value is 0. Note 
that a value of 1 will display no picture at all. Negative values will result in 
the picture being squeezed inward from the edge being cropped (the empty space 
between the picture and the cropped edge will be filled by the fill color of the 
shape). Positive values less than 1 will result in the remaining picture being 
stretched to fit the shape.

The default value is 0.




### See Also

* module [Aspose.Words.Drawing](../../)
* class [ImageData](../)

