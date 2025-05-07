---
title: OfficeMath.getMathRenderer method
linktitle: getMathRenderer method
articleTitle: getMathRenderer method
second_title: Aspose.Words for Node.js
description: "OfficeMath.getMathRenderer method. Creates and returns an object that can be used to render this equation into an image."
type: docs
weight: 60
url: /nodejs-net/aspose.words.math/officemath/getMathRenderer/
---

## getMathRenderer() {#default}

Creates and returns an object that can be used to render this equation into an image.


```js
getMathRenderer()
```

### Remarks

This method just invokes the [OfficeMathRenderer](../../../aspose.words.rendering/officemathrenderer/) constructor and passes
this object as a parameter.




### Returns

The renderer object for this equation.


### Examples

Shows how to render an Office Math object into an image file in the local file system.

```js
let doc = new aw.Document(base.myDir + "Office math.docx");

let officeMath = doc.getOfficeMath(0, true);

// Create an "ImageSaveOptions" object to pass to the node renderer's "Save" method to modify
// how it renders the OfficeMath node into an image.
let saveOptions = new aw.Saving.ImageSaveOptions(aw.SaveFormat.Png);

// Set the "Scale" property to 5 to render the object to five times its original size.
saveOptions.scale = 5;

officeMath.getMathRenderer().save(base.artifactsDir + "Shape.RenderOfficeMath.png", saveOptions);
```

### See Also

* module [Aspose.Words.Math](../../)
* class [OfficeMath](../)

