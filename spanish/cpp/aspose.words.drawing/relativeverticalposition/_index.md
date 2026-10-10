---
title: "Aspose::Words::Drawing::RelativeVerticalPosition enum"
linktitle: "RelativeVerticalPosition"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::RelativeVerticalPosition enum. Especifica a qué es relativa la posición vertical de una forma o marco de texto en C++."
type: docs
weight: 34000
url: /es/cpp/aspose.words.drawing/relativeverticalposition/
---
## RelativeVerticalPosition enum


Especifica a qué es relativa la posición vertical de una forma o marco de texto.

```cpp
enum class RelativeVerticalPosition
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Margen | 0 | Especifica que la posición vertical debe ser relativa a los márgenes de la página. |
| Page | 1 | El objeto está posicionado relativo al borde superior de la página. |
| Paragraph | 2 | El objeto está posicionado relativo a la parte superior del párrafo que contiene el ancla. |
| Línea | 3 | Sin documentación. |
| TopMargin | 4 | Especifica que la posición vertical debe ser relativa al margen superior de la página actual. |
| BottomMargin | 5 | Especifica que la posición vertical debe ser relativa al margen inferior de la página actual. |
| InsideMargin | 6 | Especifica que la posición vertical debe ser relativa al margen interior de la página actual. |
| OutsideMargin | 7 | Especifica que la posición vertical debe ser relativa al margen exterior de la página actual. |
| TableDefault | n/a | El valor predeterminado es [Margin](./). |
| TextFrameDefault | n/a | El valor predeterminado es [Paragraph](./). |


## Ejemplos



Muestra cómo insertar una imagen y usarla como marca de agua.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserta la imagen en el encabezado para que sea visible en cada página.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);

// Coloca la imagen en el centro de la página.
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_Left((builder->get_PageSetup()->get_PageWidth() - shape->get_Width()) / 2);
shape->set_Top((builder->get_PageSetup()->get_PageHeight() - shape->get_Height()) / 2);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertWatermark.docx");
```


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
