---
title: "Aspose::Words::Saving::ImageSavingArgs::get_CurrentShape-Methode"
linktitle: "get_CurrentShape"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::ImageSavingArgs::get_CurrentShape-Methode. Gibt das ShapeBase-Objekt zurück, das der Form oder Gruppierung entspricht, die in C++ gespeichert werden soll."
type: docs
weight: 2000
url: /de/cpp/aspose.words.saving/imagesavingargs/get_currentshape/
---
## ImageSavingArgs::get_CurrentShape method


Gibt das [ShapeBase](../../../aspose.words.drawing/shapebase/) Objekt zurück, das der Form oder Gruppierung entspricht, die gespeichert werden soll.

```cpp
System::SharedPtr<Aspose::Words::Drawing::ShapeBase> Aspose::Words::Saving::ImageSavingArgs::get_CurrentShape() const
```

## Hinweise


[IImageSavingCallback](../../iimagesavingcallback/) can be fired while saving either a shape or a group shape. That's why the property has [ShapeBase](../../../aspose.words.drawing/shapebase/) type. You can check whether it's a group shape comparing [ShapeType](../../../aspose.words.drawing/shapebase/get_shapetype/) with [Group](../../../aspose.words.drawing/shapetype/) or by casting it to one of derived classes: [Shape](../../../aspose.words.drawing/shape/) or [GroupShape](../../../aspose.words.drawing/groupshape/).

Aspose.Words verwendet den Dateinamen des Dokuments und eine eindeutige Nummer, um für jedes im Dokument gefundene Bild einen eindeutigen Dateinamen zu erzeugen. Sie können die Eigenschaft [CurrentShape](./) verwenden, um einen \"besseren\" Dateinamen zu generieren, indem Sie Formeigenschaften wie [Title](../../../aspose.words.drawing/imagedata/get_title/) (nur Form), [SourceFullName](../../../aspose.words.drawing/imagedata/get_sourcefullname/) (nur Form) und [Name](../../../aspose.words.drawing/shapebase/get_name/) untersuchen. Natürlich können Sie Dateinamen anhand anderer Eigenschaften oder Kriterien erstellen, beachten Sie jedoch, dass Unterdateinamen innerhalb des Exportvorgangs eindeutig sein müssen.

Einige Bilder im Dokument können nicht verfügbar sein. Um die Bildverfügbarkeit zu prüfen, verwenden Sie die Eigenschaft [IsImageAvailable](../get_isimageavailable/).
## Siehe auch

* Class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* Class [ImageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
