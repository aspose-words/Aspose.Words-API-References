---
title: "Método Aspose::Words::PageSetup::get_PageHeight"
linktitle: "get_PageHeight"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::PageSetup::get_PageHeight. Devuelve o establece la altura de la página en puntos en C++."
type: docs
weight: 33000
url: /es/cpp/aspose.words/pagesetup/get_pageheight/
---
## PageSetup::get_PageHeight method


Devuelve o establece la altura de la página en puntos.

```cpp
double Aspose::Words::PageSetup::get_PageHeight()
```


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

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
