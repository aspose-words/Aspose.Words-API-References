---
title: "Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalPosition método"
linktitle: "get_RelativeVerticalPosition"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalPosition método. Especifica a qué se posiciona verticalmente la forma en C++."
type: docs
weight: 43000
url: /es/cpp/aspose.words.drawing/shapebase/get_relativeverticalposition/
---
## ShapeBase::get_RelativeVerticalPosition method


Especifica respecto a qué se posiciona verticalmente la forma.

```cpp
Aspose::Words::Drawing::RelativeVerticalPosition Aspose::Words::Drawing::ShapeBase::get_RelativeVerticalPosition()
```

## Observaciones


El valor predeterminado es [Paragraph](../../relativeverticalposition/).

Solo tiene efecto para formas flotantes de nivel superior.

## Ejemplos



Muestra cómo insertar una imagen flotante en el centro de una página.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserta una imagen flotante que aparecerá detrás del texto superpuesto y alinéala al centro de la página.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
shape->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Center);

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPageCenter.docx");
```

## Ver también

* Enum [RelativeVerticalPosition](../../relativeverticalposition/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
