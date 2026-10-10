---
title: "Aspose::Words::PageSetup::get_Gutter método"
linktitle: "get_Gutter"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::PageSetup::get_Gutter método. Obtiene o establece la cantidad de espacio adicional añadido al margen para la encuadernación del documento en C++."
type: docs
weight: 18000
url: /es/cpp/aspose.words/pagesetup/get_gutter/
---
## PageSetup::get_Gutter method


Obtiene o establece la cantidad de espacio adicional añadido al margen para la encuadernación del documento.

```cpp
double Aspose::Words::PageSetup::get_Gutter()
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


Muestra cómo configurar un documento que se puede imprimir como un pliegue de libro.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Inserte texto que abarque 16 páginas.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"My Booklet:");

for (int32_t i = 0; i < 15; i++)
{
    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
    builder->Write(System::String::Format(u"Booklet face #{0}", i));
}

// Configure la propiedad "PageSetup" de la primera sección para imprimir el documento en forma de pliegue de libro.
// Cuando imprimimos este documento a doble cara, podemos tomar las páginas para apilarlas
// y doblarlas todas por la mitad de una vez. El contenido del documento se alineará en un pliegue de libro.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::BookFoldPrinting);

// Solo podemos especificar el número de hojas en múltiplos de 4.
pageSetup->set_SheetsPerBooklet(4);

doc->Save(get_ArtifactsDir() + u"PageSetup.Booklet.docx");
```

## Ver también

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
