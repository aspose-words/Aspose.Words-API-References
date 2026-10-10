---
title: "Aspose::Words::MailMerging::ImageFieldMergingArgs::get_Shape método"
linktitle: "get_Shape"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::MailMerging::ImageFieldMergingArgs::get_Shape método. Especifica la forma que el motor de combinación de correspondencia debe insertar en el documento en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words.mailmerging/imagefieldmergingargs/get_shape/
---
## ImageFieldMergingArgs::get_Shape method


Especifica la forma que el motor de combinación de correspondencia debe insertar en el documento.

```cpp
const System::SharedPtr<Aspose::Words::Drawing::Shape> & Aspose::Words::MailMerging::ImageFieldMergingArgs::get_Shape() const
```

## Observaciones


Cuando se especifica esta propiedad, el motor de combinación de correspondencia ignora todas las demás propiedades como [ImageFileName](../get_imagefilename/) o [ImageStream](../get_imagestream/) y simplemente inserta la forma en el documento.

Utilice esta propiedad para controlar completamente el proceso de combinación de un campo de imagen. Por ejemplo, puede especificar [WrapType](../../../aspose.words.drawing/shapebase/get_wraptype/) u otra propiedad de forma para afinar el nodo resultante. Sin embargo, tenga en cuenta que usted es responsable de proporcionar el contenido de la forma.
## Ver también

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [ImageFieldMergingArgs](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
