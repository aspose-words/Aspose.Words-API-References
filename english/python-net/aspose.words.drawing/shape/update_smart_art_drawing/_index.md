---
title: Shape.update_smart_art_drawing method
linktitle: update_smart_art_drawing method
articleTitle: update_smart_art_drawing method
second_title: Aspose.Words for Python
description: "Shape.update_smart_art_drawing method. Updates SmartArt pre-rendered drawing by using Aspose.Words's SmartArt cold rendering engine."
type: docs
weight: 270
url: /python-net/aspose.words.drawing/shape/update_smart_art_drawing/
---

## update_smart_art_drawing() {#default}

Updates SmartArt pre-rendered drawing by using Aspose.Words's SmartArt cold rendering engine.


```python
def update_smart_art_drawing(self):
    ...
```

### Remarks

Microsoft Word generates and saves the pre-rendered drawing along with SmartArt object. However,
if the document is saved by other applications, the pre-rendered SmartArt drawing may be missing or incorrect.
If pre-rendered drawing is available then Aspose.Words uses it to render the SmartArt object.
If pre-rendered drawing is missing then Aspose.Words uses its own SmartArt cold rendering engine to render the
SmartArt object.
If pre-rendered drawing is incorrect then it is required to call this method to invoke the SmartArt cold
rendering engine.


### See Also

* module [aspose.words.drawing](../../)
* class [Shape](../)

