---
title: "Aspose::Words::Saving::ImageSaveOptions::get_Scale método"
linktitle: "get_Scale"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::ImageSaveOptions::get_Scale método. Obtiene o establece el factor de zoom para las imágenes generadas en C++."
type: docs
weight: 14000
url: /es/cpp/aspose.words.saving/imagesaveoptions/get_scale/
---
## ImageSaveOptions::get_Scale method


Obtiene o establece el factor de zoom para las imágenes generadas.

```cpp
float Aspose::Words::Saving::ImageSaveOptions::get_Scale() const
```


## Ejemplos



Muestra cómo editar la imagen mientras Aspose.Words convierte un documento a una.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Cuando guardamos el documento como una imagen, podemos pasar un objeto SaveOptions a
// edita la imagen mientras la operación de guardado la renderiza.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
// Podemos ajustar estas propiedades para cambiar el brillo y el contraste de la imagen.
// Ambas están en una escala de 0-1 y su valor predeterminado es 0.5.
options->set_ImageBrightness(0.3f);
options->set_ImageContrast(0.7f);
// Podemos ajustar la resolución horizontal y vertical con estas propiedades.
// Esto afectará las dimensiones de la imagen.
// El valor predeterminado para estas propiedades es 96.0, para una resolución de 96 dpi.
options->set_HorizontalResolution(72.f);
options->set_VerticalResolution(72.f);
// Podemos escalar la imagen usando esta propiedad. El valor predeterminado es 1.0, para un escalado del 100%.
// Podemos usar esta propiedad para anular cualquier cambio en las dimensiones de la imagen que causaría cambiar la resolución.
options->set_Scale(96.f / 72.f);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.EditImage.png", options);
```


Muestra cómo renderizar un objeto de Office [Math](../../../aspose.words.math/) en un archivo de imagen en el sistema de archivos local.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto math = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));

// Cree un objeto "ImageSaveOptions" para pasar al método "Save" del renderizador de nodos y modificar
// cómo renderiza el nodo OfficeMath en una imagen.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);

// Establezca la propiedad "Scale" a 5 para renderizar el objeto a cinco veces su tamaño original.
saveOptions->set_Scale(5.0f);

math->GetMathRenderer()->Save(get_ArtifactsDir() + u"Shape.RenderOfficeMath.png", saveOptions);
```

## Ver también

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
