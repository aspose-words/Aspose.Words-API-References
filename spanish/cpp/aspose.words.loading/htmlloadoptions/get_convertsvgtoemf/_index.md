---
title: "Aspose::Words::Loading::HtmlLoadOptions::get_ConvertSvgToEmf método"
linktitle: "get_ConvertSvgToEmf"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Loading::HtmlLoadOptions::get_ConvertSvgToEmf método. Obtiene o establece un valor que indica si convertir las imágenes SVG cargadas al formato EMF. El valor predeterminado es false y, si es posible, las imágenes SVG cargadas se almacenan tal cual sin conversión en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.loading/htmlloadoptions/get_convertsvgtoemf/
---
## HtmlLoadOptions::get_ConvertSvgToEmf method


Obtiene o establece un valor que indica si se convierten las imágenes SVG cargadas al formato EMF. El valor predeterminado es **false** y, si es posible, las imágenes SVG cargadas se almacenan tal cual sin conversión.

```cpp
bool Aspose::Words::Loading::HtmlLoadOptions::get_ConvertSvgToEmf() const
```

## Observaciones


Las versiones más recientes de MS Word admiten imágenes SVG de forma nativa. Si la versión de MS Word especificada en las opciones de carga admite SVG, Aspose.Words almacenará las imágenes SVG tal cual sin conversión. Si SVG no es compatible, las imágenes SVG cargadas se convertirán al formato EMF.

Sin embargo, si esta opción se establece en **true**, Aspose.Words convertirá las imágenes SVG cargadas a EMF incluso si las imágenes SVG son compatibles con la versión especificada de MS Word.

## Ejemplos



Muestra cómo convertir objetos SVG a un formato diferente al guardar documentos HTML.
```cpp
System::String html = u"<html>\r\n                    <svg xmlns='http://www.w3.org/2000/svg' width='500' height='40' viewBox='0 0 500 40'>\r\n                        <text x='0' y='35' font-family='Verdana' font-size='35'>Hello world!</text>\r\n                    </svg>\r\n                </html>";

// Use 'ConvertSvgToEmf' para revertir el comportamiento heredado
// donde todas las imágenes SVG cargadas desde un documento HTML se convertían a EMF.
// Ahora las imágenes SVG se cargan sin conversión
// si la versión de MS Word especificada en las opciones de carga admite imágenes SVG de forma nativa.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
loadOptions->set_ConvertSvgToEmf(true);

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(html)), loadOptions);

// Este documento contiene un elemento <svg> en forma de texto.
// Cuando guardamos el documento en HTML, podemos pasar un objeto SaveOptions
// para determinar cómo maneja la operación de guardado este objeto.
// Estableciendo la propiedad "MetafileFormat" a "HtmlMetafileFormat.Png" para convertirla en una imagen PNG.
// Estableciendo la propiedad "MetafileFormat" a "HtmlMetafileFormat.Svg" lo preserva como un objeto SVG.
// Estableciendo la propiedad "MetafileFormat" a "HtmlMetafileFormat.EmfOrWmf" para convertirla en un metarchivo.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_MetafileFormat(htmlMetafileFormat);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.MetafileFormat.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.MetafileFormat.html");

switch (htmlMetafileFormat)
{
    case Aspose::Words::Saving::HtmlMetafileFormat::Png:
        ASSERT_TRUE(outDocContents.Contains(System::String(u"<p style=\"margin-top:0pt; margin-bottom:0pt\">") + u"<img src=\"HtmlSaveOptions.MetafileFormat.001.png\" width=\"500\" height=\"40\" alt=\"\" " + u"style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" + u"</p>"));
        break;

    case Aspose::Words::Saving::HtmlMetafileFormat::Svg:
        ASSERT_TRUE(outDocContents.Contains(System::String(u"<span style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\">") + u"<svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" version=\"1.1\" width=\"499\" height=\"40\">"));
        break;

    case Aspose::Words::Saving::HtmlMetafileFormat::EmfOrWmf:
        ASSERT_TRUE(outDocContents.Contains(System::String(u"<p style=\"margin-top:0pt; margin-bottom:0pt\">") + u"<img src=\"HtmlSaveOptions.MetafileFormat.001.emf\" width=\"500\" height=\"40\" alt=\"\" " + u"style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" + u"</p>"));
        break;

}
```

## Ver también

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
