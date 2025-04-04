---
title: ImageData.cropBottom property
linktitle: cropBottom property
articleTitle: cropBottom property
second_title: Aspose.Words for Node.js
description: "ImageData.cropBottom property. Defines the fraction of picture removal from the bottom side."
type: docs
weight: 60
url: /nodejs-net/aspose.words.drawing/imagedata/cropBottom/
---

## ImageData.cropBottom property

Defines the fraction of picture removal from the bottom side.


```js
get cropBottom(): number
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

