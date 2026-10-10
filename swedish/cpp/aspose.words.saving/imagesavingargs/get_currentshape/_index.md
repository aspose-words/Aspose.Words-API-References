---
title: "Aspose::Words::Saving::ImageSavingArgs::get_CurrentShape‑metod"
linktitle: "get_CurrentShape"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::ImageSavingArgs::get_CurrentShape‑metod. Hämtar ShapeBase‑objektet som motsvarar den form eller gruppform som ska sparas i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.saving/imagesavingargs/get_currentshape/
---
## ImageSavingArgs::get_CurrentShape method


Hämtar [ShapeBase](../../../aspose.words.drawing/shapebase/)‑objektet som motsvarar den form eller gruppform som ska sparas.

```cpp
System::SharedPtr<Aspose::Words::Drawing::ShapeBase> Aspose::Words::Saving::ImageSavingArgs::get_CurrentShape() const
```

## Anmärkningar


[IImageSavingCallback](../../iimagesavingcallback/) can be fired while saving either a shape or a group shape. That's why the property has [ShapeBase](../../../aspose.words.drawing/shapebase/) type. You can check whether it's a group shape comparing [ShapeType](../../../aspose.words.drawing/shapebase/get_shapetype/) with [Group](../../../aspose.words.drawing/shapetype/) or by casting it to one of derived classes: [Shape](../../../aspose.words.drawing/shape/) or [GroupShape](../../../aspose.words.drawing/groupshape/).

Aspose.Words använder dokumentfilens namn och ett unikt nummer för att generera unika filnamn för varje bild som finns i dokumentet. Du kan använda egenskapen [CurrentShape](./) för att skapa ett "bättre" filnamn genom att undersöka formens egenskaper såsom [Title](../../../aspose.words.drawing/imagedata/get_title/) (endast Form), [SourceFullName](../../../aspose.words.drawing/imagedata/get_sourcefullname/) (endast Form) och [Name](../../../aspose.words.drawing/shapebase/get_name/). Naturligtvis kan du konstruera filnamn med andra egenskaper eller kriterier, men observera att underordnade filnamn måste vara unika inom exportoperationen.

Vissa bilder i dokumentet kan vara otillgängliga. För att kontrollera bildens tillgänglighet, använd egenskapen [IsImageAvailable](../get_isimageavailable/).
## Se även

* Class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* Class [ImageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
