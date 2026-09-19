---
title: "Metodo Aspose::Words::Saving::ImageSavingArgs::get_CurrentShape"
linktitle: "get_CurrentShape"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::ImageSavingArgs::get_CurrentShape. Restituisce l'oggetto ShapeBase corrispondente alla forma o al gruppo di forme che sta per essere salvato in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.saving/imagesavingargs/get_currentshape/
---
## ImageSavingArgs::get_CurrentShape method


Restituisce l'oggetto [ShapeBase](../../../aspose.words.drawing/shapebase/) corrispondente alla forma o al gruppo di forme che sta per essere salvato.

```cpp
System::SharedPtr<Aspose::Words::Drawing::ShapeBase> Aspose::Words::Saving::ImageSavingArgs::get_CurrentShape() const
```

## Note


[IImageSavingCallback](../../iimagesavingcallback/) can be fired while saving either a shape or a group shape. That's why the property has [ShapeBase](../../../aspose.words.drawing/shapebase/) type. You can check whether it's a group shape comparing [ShapeType](../../../aspose.words.drawing/shapebase/get_shapetype/) with [Group](../../../aspose.words.drawing/shapetype/) or by casting it to one of derived classes: [Shape](../../../aspose.words.drawing/shape/) or [GroupShape](../../../aspose.words.drawing/groupshape/).

Aspose.Words utilizza il nome del file del documento e un numero univoco per generare un nome file unico per ogni immagine trovata nel documento. È possibile utilizzare la proprietà [CurrentShape](./) per generare un nome file "migliore" esaminando le proprietà della forma come [Title](../../../aspose.words.drawing/imagedata/get_title/) (solo forma), [SourceFullName](../../../aspose.words.drawing/imagedata/get_sourcefullname/) (solo forma) e [Name](../../../aspose.words.drawing/shapebase/get_name/). Naturalmente è possibile creare nomi file usando qualsiasi altra proprietà o criterio, ma si noti che i nomi file secondari devono essere unici all'interno dell'operazione di esportazione.

Alcune immagini nel documento possono non essere disponibili. Per verificare la disponibilità delle immagini, utilizzare la proprietà [IsImageAvailable](../get_isimageavailable/).
## Vedi anche

* Class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* Class [ImageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
