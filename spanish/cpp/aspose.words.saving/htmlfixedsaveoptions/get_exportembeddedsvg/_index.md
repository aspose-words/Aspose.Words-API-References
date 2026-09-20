---
title: "Método Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedSvg"
linktitle: "get_ExportEmbeddedSvg"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedSvg. Especifica si los recursos SVG deben incrustarse en el documento Html. El valor predeterminado es true en C++."
type: docs
weight: 8000
url: /es/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportembeddedsvg/
---
## HtmlFixedSaveOptions::get_ExportEmbeddedSvg method


Especifica si los recursos SVG deben incrustarse en el documento Html. El valor predeterminado es **true**.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedSvg() const
```


## Ejemplos



Muestra cómo determinar dónde almacenar los objetos SVG al exportar un documento a Html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

// Cuando exportamos un documento con objetos SVG a .html,
// Aspose.Words puede colocar estos objetos en dos ubicaciones posibles.
// Establecer la bandera "ExportEmbeddedSvg" a "true" incrustará todos los datos sin procesar de los objetos SVG
// dentro del HTML de salida, dentro de etiquetas <image>.
// Establecer esta bandera a "false" creará un archivo en el sistema de archivos local para cada objeto SVG.
// El HTML enlazará a cada archivo usando el atributo "data" de una etiqueta <object>.
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportEmbeddedSvg(exportSvgs);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedSvgs.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedSvgs.html");

if (exportSvgs)
{
    ASSERT_FALSE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001.svg"));
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"<image id=\"image004\" xlink:href=.+/>")->get_Success());
}
else
{
    ASSERT_TRUE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001.svg"));
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"<object type=\"image/svg[+]xml\" data=\"HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001[.]svg\"></object>")->get_Success());
}
```

## Ver también

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
