---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedCss método"
linktitle: "get_ExportEmbeddedCss"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedCss método. Especifica si el CSS (Cascading Style Sheet) debe incrustarse en el documento Html en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportembeddedcss/
---
## HtmlFixedSaveOptions::get_ExportEmbeddedCss method


Especifica si el CSS (Cascading [Style](../../../aspose.words/style/) Sheet) debe incrustarse en el documento Html.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedCss() const
```


## Ejemplos



Muestra cómo determinar dónde almacenar las hojas de estilo CSS al exportar un documento a Html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Cuando exportamos un documento a html, Aspose.Words también creará una hoja de estilo CSS para formatear el documento.
// Establecer la bandera "ExportEmbeddedCss" a "true" guarda la hoja de estilo CSS en un archivo .css,
// y enlaza el archivo desde el documento html usando un elemento <link>.
// Establecer la bandera a "false" incrustará la hoja de estilo CSS dentro del documento Html,
// lo que creará un solo archivo en lugar de dos.
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportEmbeddedCss(exportEmbeddedCss);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedCss.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedCss.html");

if (exportEmbeddedCss)
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"<style type=\"text/css\">")->get_Success());
    ASSERT_FALSE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedCss/styles.css"));
}
else
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"<link rel=\"stylesheet\" type=\"text/css\" href=\"HtmlFixedSaveOptions[.]ExportEmbeddedCss/styles[.]css\" media=\"all\" />")->get_Success());
    ASSERT_TRUE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedCss/styles.css"));
}
```

## Ver también

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
