---
title: "Aspose::Words::Saving::ImageSavingArgs::get_CurrentShape método"
linktitle: "get_CurrentShape"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::ImageSavingArgs::get_CurrentShape método. Obtiene el objeto ShapeBase correspondiente a la forma o grupo de formas que está a punto de guardarse en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.saving/imagesavingargs/get_currentshape/
---
## ImageSavingArgs::get_CurrentShape method


Obtiene el objeto [ShapeBase](../../../aspose.words.drawing/shapebase/) correspondiente a la forma o grupo de formas que está a punto de guardarse.

```cpp
System::SharedPtr<Aspose::Words::Drawing::ShapeBase> Aspose::Words::Saving::ImageSavingArgs::get_CurrentShape() const
```

## Observaciones


[IImageSavingCallback](../../iimagesavingcallback/) can be fired while saving either a shape or a group shape. That's why the property has [ShapeBase](../../../aspose.words.drawing/shapebase/) type. You can check whether it's a group shape comparing [ShapeType](../../../aspose.words.drawing/shapebase/get_shapetype/) with [Group](../../../aspose.words.drawing/shapetype/) or by casting it to one of derived classes: [Shape](../../../aspose.words.drawing/shape/) or [GroupShape](../../../aspose.words.drawing/groupshape/).

Aspose.Words utiliza el nombre del archivo del documento y un número único para generar un nombre de archivo único para cada imagen encontrada en el documento. Puede usar la propiedad [CurrentShape](./) para generar un nombre de archivo "mejor" examinando las propiedades de la forma como [Title](../../../aspose.words.drawing/imagedata/get_title/) (solo forma), [SourceFullName](../../../aspose.words.drawing/imagedata/get_sourcefullname/) (solo forma) y [Name](../../../aspose.words.drawing/shapebase/get_name/). Por supuesto, puede construir nombres de archivo usando cualquier otra propiedad o criterio, pero tenga en cuenta que los nombres de archivo subsidiarios deben ser únicos dentro de la operación de exportación.

Algunas imágenes en el documento pueden no estar disponibles. Para comprobar la disponibilidad de la imagen use la propiedad [IsImageAvailable](../get_isimageavailable/).
## Ver también

* Class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* Class [ImageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
