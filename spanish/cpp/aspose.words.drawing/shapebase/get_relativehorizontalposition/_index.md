---
title: "Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalPosition método"
linktitle: "get_RelativeHorizontalPosition"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalPosition método. Especifica respecto a qué se posiciona horizontalmente la forma en C++."
type: docs
weight: 42000
url: /es/cpp/aspose.words.drawing/shapebase/get_relativehorizontalposition/
---
## ShapeBase::get_RelativeHorizontalPosition method


Especifica respecto a qué se posiciona horizontalmente la forma.

```cpp
Aspose::Words::Drawing::RelativeHorizontalPosition Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalPosition()
```

## Observaciones


El valor predeterminado es [Column](../../relativehorizontalposition/).

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

* Enum [RelativeHorizontalPosition](../../relativehorizontalposition/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
