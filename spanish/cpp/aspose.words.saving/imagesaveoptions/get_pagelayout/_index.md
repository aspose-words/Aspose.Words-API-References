---
title: "Aspose::Words::Saving::ImageSaveOptions::get_PageLayout método"
linktitle: "get_PageLayout"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::ImageSaveOptions::get_PageLayout método. Obtiene o establece el diseño utilizado al renderizar varias páginas en una única salida en C++."
type: docs
weight: 9500
url: /es/cpp/aspose.words.saving/imagesaveoptions/get_pagelayout/
---
## ImageSaveOptions::get_PageLayout method


Obtiene o establece el diseño utilizado al renderizar varias páginas en una única salida.

```cpp
System::SharedPtr<Aspose::Words::Saving::MultiPageLayout> Aspose::Words::Saving::ImageSaveOptions::get_PageLayout() const
```

## Observaciones


Utilice uno de los métodos de fábrica de [MultiPageLayout](../../multipagelayout/) para configurar esta propiedad.

Para [Tiff](../../../aspose.words/saveformat/) el valor predeterminado es [TiffFrames](../../multipagelayout/tiffframes/). Para otros formatos el valor predeterminado es [SinglePage](../../multipagelayout/singlepage/).

Esta propiedad tiene efecto solo al guardar en los siguientes formatos: [Jpeg](../../../aspose.words/saveformat/), [Gif](../../../aspose.words/saveformat/), [Png](../../../aspose.words/saveformat/), [Bmp](../../../aspose.words/saveformat/), [Tiff](../../../aspose.words/saveformat/), [WebP](../)

## Ejemplos



Muestra cómo guardar el documento en una imagen JPG con configuraciones de diseño de varias páginas.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// Configura un diseño de cuadrícula con:
// - 3 columnas por fila.
// - Espaciado de 10 pts entre páginas (horizontal y vertical).
options->set_PageLayout(Aspose::Words::Saving::MultiPageLayout::Grid(3, 10.0f, 10.0f));

// Diseños alternativos:
// options.PageLayout = MultiPageLayout.Horizontal(10);
// options.PageLayout = MultiPageLayout.Vertical(10);

// Personaliza el fondo y el borde.
options->get_PageLayout()->set_BackColor(System::Drawing::Color::get_LightGray());
options->get_PageLayout()->set_BorderColor(System::Drawing::Color::get_Blue());
options->get_PageLayout()->set_BorderWidth(2.0f);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.GridLayout.jpg", options);
```

## Ver también

* Class [MultiPageLayout](../../multipagelayout/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
