---
title: "Aspose::Words::PageSetup::get_RtlGutter método"
linktitle: "get_RtlGutter"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::PageSetup::get_RtlGutter método. Obtiene o establece si Microsoft Word usa canaletas para la sección según un idioma de derecha a izquierda o de izquierda a derecha en C++."
type: docs
weight: 40000
url: /es/cpp/aspose.words/pagesetup/get_rtlgutter/
---
## PageSetup::get_RtlGutter method


Obtiene o establece si Microsoft Word usa gutters para la sección según un idioma de derecha a izquierda o de izquierda a derecha.

```cpp
bool Aspose::Words::PageSetup::get_RtlGutter()
```


## Ejemplos



Muestra cómo establecer márgenes de gutter.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Inserte texto que abarque varias páginas.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
for (int32_t i = 0; i < 6; i++)
{
    builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
}

// Un gutter agrega espacios en blanco al margen izquierdo o derecho de la página,
// lo que compensa el pliegue central de las páginas en un libro que invade el diseño de la página.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();

// Determine cuánto espacio tienen nuestras páginas para texto dentro de los márgenes y luego añada una cantidad para rellenar un margen.
ASSERT_NEAR(470.30, pageSetup->get_PageWidth() - pageSetup->get_LeftMargin() - pageSetup->get_RightMargin(), 0.01);

pageSetup->set_Gutter(100.0);

// Establezca la propiedad "RtlGutter" a "true" para colocar el gutter en una posición más adecuada para texto de derecha a izquierda.
pageSetup->set_RtlGutter(true);

// Establezca la propiedad "MultiplePages" a "MultiplePagesType.MirrorMargins" para alternar
// la posición del lado izquierdo/derecho de los márgenes en cada página.
pageSetup->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::MirrorMargins);

doc->Save(get_ArtifactsDir() + u"PageSetup.Gutter.docx");
```

## Ver también

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
