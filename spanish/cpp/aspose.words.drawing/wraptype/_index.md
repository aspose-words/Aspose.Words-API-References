---
title: "Aspose::Words::Drawing::WrapType enum"
linktitle: "WrapType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::WrapType enum. Especifica cómo se ajusta el texto alrededor de una forma o imagen en C++."
type: docs
weight: 45000
url: /es/cpp/aspose.words.drawing/wraptype/
---
## WrapType enum


Especifica cómo se ajusta el texto alrededor de una forma o imagen.

```cpp
enum class WrapType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | 3 | No hay ajuste de texto alrededor de la forma. La forma se coloca detrás o delante del texto. |
| En línea | 0 | La forma permanece en la misma capa que el texto y se trata como un carácter. |
| TopBottom | 1 | El texto se detiene en la parte superior de la forma y vuelve a comenzar en la línea debajo de la forma. |
| Square | 2 | Ajusta el texto alrededor de todos los lados del cuadro delimitador cuadrado de la forma. |
| Tight | 4 | Ajusta estrechamente alrededor de los bordes de la forma, en lugar de ajustarse alrededor del cuadro delimitador. |
| Through | 5 | Igual que Tight, pero ajusta dentro de cualquier parte de la forma que esté abierta. |


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
