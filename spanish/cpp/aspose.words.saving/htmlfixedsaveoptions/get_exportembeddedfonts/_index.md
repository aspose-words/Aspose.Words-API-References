---
title: "Método Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedFonts"
linktitle: "get_ExportEmbeddedFonts"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedFonts. Especifica si las fuentes deben incrustarse en el documento Html en formato Base64. Tenga en cuenta que establecer esta bandera puede aumentar significativamente el tamaño del archivo Html de salida en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportembeddedfonts/
---
## HtmlFixedSaveOptions::get_ExportEmbeddedFonts method


Especifica si las fuentes deben incrustarse en el documento Html en formato Base64. Nota: activar esta opción puede aumentar significativamente el tamaño del archivo Html de salida.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedFonts() const
```


## Ejemplos



Muestra cómo determinar dónde almacenar fuentes incrustadas al exportar un documento a Html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

// Cuando exportamos un documento con fuentes incrustadas a .html,
// Aspose.Words puede colocar las fuentes en dos ubicaciones posibles.
// Establecer la bandera "ExportEmbeddedFonts" a "true" almacenará los datos sin procesar de las fuentes incrustadas dentro de la hoja de estilos CSS,
// en la propiedad "url" de la regla "@font-face". Esto puede crear un archivo de hoja de estilos CSS enorme
// y reducir la cantidad de archivos externos que esta conversión HTML creará.
// Establecer esta bandera a "false" creará un archivo para cada fuente.
// La hoja de estilo CSS enlazará a cada archivo de fuente usando la propiedad "url" de la regla "@font-face".
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportEmbeddedFonts(exportEmbeddedFonts);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedFonts.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedFonts/styles.css");

if (exportEmbeddedFonts)
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], url[(].+[)] format[(]'woff'[)]; }")->get_Success());
    ASSERT_EQ(0, System::IO::Directory::GetFiles(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedFonts")->LINQ_Count(static_cast<System::Func<System::String, bool>>(static_cast<std::function<bool(System::String f)>>([](System::String f) -> bool
    {
        return f.EndsWith(u".woff");
    }))));
}
else
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], url[(]'font001[.]woff'[)] format[(]'woff'[)]; }")->get_Success());
    ASSERT_EQ(2, System::IO::Directory::GetFiles(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedFonts")->LINQ_Count(static_cast<System::Func<System::String, bool>>(static_cast<std::function<bool(System::String f)>>([](System::String f) -> bool
    {
        return f.EndsWith(u".woff");
    }))));
}
```

## Ver también

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
