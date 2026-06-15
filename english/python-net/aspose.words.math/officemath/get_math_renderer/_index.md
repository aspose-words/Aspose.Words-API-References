---
title: OfficeMath.get_math_renderer method
linktitle: get_math_renderer method
articleTitle: get_math_renderer method
second_title: Aspose.Words for Python
description: "OfficeMath.get_math_renderer method. Creates and returns an object that can be used to render this equation into an image."
type: docs
weight: 90
url: /python-net/aspose.words.math/officemath/get_math_renderer/
---

## get_math_renderer() {#default}

Creates and returns an object that can be used to render this equation into an image.


```python
def get_math_renderer(self):
    ...
```

### Remarks

This method just invokes the [OfficeMathRenderer](../../../aspose.words.rendering/officemathrenderer/) constructor and passes
this object as a parameter.




### Returns

The renderer object for this equation.


### Examples

Shows how to render an Office Math object into an image file in the local file system.

```python
from api_example_base import ApiExampleBase, MY_DIR, ARTIFACTS_DIR, GOLDS_DIR, TEMP_DIR, IMAGE_DIR, FONTS_DIR
import aspose.words as aw
doc = aw.Document(file_name=MY_DIR + 'Office math.docx')
math = doc.get_child(aw.NodeType.OFFICE_MATH, 0, True).as_office_math()
# Create an "ImageSaveOptions" object to pass to the node renderer's "Save" method to modify
# how it renders the OfficeMath node into an image.
save_options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
# Set the "Scale" property to 5 to render the object to five times its original size.
save_options.scale = 5
math.get_math_renderer().save(file_name=ARTIFACTS_DIR + 'Shape.RenderOfficeMath.png', save_options=save_options)
```

### See Also

* module [aspose.words.math](../../)
* class [OfficeMath](../)

