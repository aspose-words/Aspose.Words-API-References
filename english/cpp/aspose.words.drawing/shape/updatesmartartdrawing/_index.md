---
title: Aspose::Words::Drawing::Shape::UpdateSmartArtDrawing method
linktitle: UpdateSmartArtDrawing
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Shape::UpdateSmartArtDrawing method. Updates SmartArt pre-rendered drawing by using Aspose.Words''s SmartArt cold rendering engine in C++.'
type: docs
weight: 33000
url: /cpp/aspose.words.drawing/shape/updatesmartartdrawing/
---
## Shape::UpdateSmartArtDrawing method


Updates SmartArt pre-rendered drawing by using Aspose.Words's SmartArt cold rendering engine.

```cpp
void Aspose::Words::Drawing::Shape::UpdateSmartArtDrawing()
```

## Remarks

 Microsoft Word generates and saves the pre-rendered drawing along with SmartArt object. However, if the document is saved by other applications, the pre-rendered SmartArt drawing may be missing or incorrect. If pre-rendered drawing is available then Aspose.Words uses it to render the SmartArt object. If pre-rendered drawing is missing then Aspose.Words uses its own SmartArt cold rendering engine to render the SmartArt object. If pre-rendered drawing is incorrect then it is required to call this method to invoke the SmartArt cold rendering engine. 
## See Also

* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
