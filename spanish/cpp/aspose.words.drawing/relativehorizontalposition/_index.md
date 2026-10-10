---
title: "Aspose::Words::Drawing::RelativeHorizontalPosition enum"
linktitle: "RelativeHorizontalPosition"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::RelativeHorizontalPosition enum. Especifica a qué es relativa la posición horizontal de una forma o marco de texto en C++."
type: docs
weight: 33000
url: /es/cpp/aspose.words.drawing/relativehorizontalposition/
---
## RelativeHorizontalPosition enum


Especifica a qué es relativa la posición horizontal de una forma o marco de texto.

```cpp
enum class RelativeHorizontalPosition
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Margen | 0 | Especifica que la posición horizontal debe ser relativa a los márgenes de la página. |
| Page | 1 | El objeto está posicionado relativo al borde izquierdo de la página. |
| Columna | 2 | El objeto está posicionado relativo al lado izquierdo de la columna. |
| Character | 3 | El objeto está posicionado relativo al lado izquierdo del párrafo. |
| LeftMargin | 4 | Especifica que la posición horizontal debe ser relativa al margen izquierdo de la página. |
| RightMargin | 5 | Especifica que la posición horizontal debe ser relativa al margen derecho de la página. |
| InsideMargin | 6 | Especifica que la posición horizontal debe ser relativa al margen interior de la página actual (el margen izquierdo en páginas impares, el derecho en páginas pares). |
| OutsideMargin | 7 | Especifica que la posición horizontal debe ser relativa al margen exterior de la página actual (el margen derecho en páginas impares, el izquierdo en páginas pares). |
| Default | n/a | El valor predeterminado es [Column](./). |


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
