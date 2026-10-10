---
title: "Aspose::Words::DocumentBuilder::MoveToHeaderFooter método"
linktitle: "MoveToHeaderFooter"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DocumentBuilder::MoveToHeaderFooter método. Mueve el cursor al inicio de un encabezado o pie de página en la sección actual en C++."
type: docs
weight: 57000
url: /es/cpp/aspose.words/documentbuilder/movetoheaderfooter/
---
## DocumentBuilder::MoveToHeaderFooter method


Mueve el cursor al comienzo de un encabezado o pie de página en la sección actual.

```cpp
void Aspose::Words::DocumentBuilder::MoveToHeaderFooter(Aspose::Words::HeaderFooterType headerFooterType)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| headerFooterType | Aspose::Words::HeaderFooterType | Especifica el encabezado o pie de página al que moverse. |
## Observaciones


Después de mover el cursor a un encabezado o pie de página, puedes usar el resto de los métodos de [DocumentBuilder](../) para modificar el contenido del encabezado o pie de página.

Si deseas crear encabezados y pies de página diferentes para la primera página, debes establecer [DifferentFirstPageHeaderFooter](../../pagesetup/get_differentfirstpageheaderfooter/).

Si deseas crear encabezados y pies de página diferentes para páginas pares e impares, debes establecer [OddAndEvenPagesHeaderFooter](../../pagesetup/get_oddandevenpagesheaderfooter/).

Utiliza [MoveToSection()](../movetosection/) para salir del encabezado y pasar al texto principal.

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

## Ver también

* Enum [HeaderFooterType](../../headerfootertype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
