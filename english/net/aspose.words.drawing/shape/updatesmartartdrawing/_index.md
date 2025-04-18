---
title: Shape.UpdateSmartArtDrawing
linktitle: UpdateSmartArtDrawing
articleTitle: UpdateSmartArtDrawing
second_title: Aspose.Words for .NET
description: Enhance your documents with the Shape UpdateSmartArtDrawing method, utilizing Aspose.Words' advanced SmartArt rendering for stunning visuals.
type: docs
weight: 280
url: /net/aspose.words.drawing/shape/updatesmartartdrawing/
---
## Shape.UpdateSmartArtDrawing method

Updates SmartArt pre-rendered drawing by using Aspose.Words's SmartArt cold rendering engine.

```csharp
public void UpdateSmartArtDrawing()
```

## Remarks

Microsoft Word generates and saves the pre-rendered drawing along with SmartArt object. However, if the document is saved by other applications, the pre-rendered SmartArt drawing may be missing or incorrect. If pre-rendered drawing is available then Aspose.Words uses it to render the SmartArt object. If pre-rendered drawing is missing then Aspose.Words uses its own SmartArt cold rendering engine to render the SmartArt object. If pre-rendered drawing is incorrect then it is required to call this method to invoke the SmartArt cold rendering engine.

### See Also

* class [Shape](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
