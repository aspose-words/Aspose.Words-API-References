---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedCss metodo"
linktitle: "get_ExportEmbeddedCss"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedCss metodo. Specifica se il CSS (Cascading Style Sheet) deve essere incorporato nel documento Html in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportembeddedcss/
---
## HtmlFixedSaveOptions::get_ExportEmbeddedCss method


Specifica se il CSS (Cascading [Style](../../../aspose.words/style/) Sheet) deve essere incorporato nel documento Html.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedCss() const
```


## Esempi



Mostra come determinare dove memorizzare i fogli di stile CSS durante l'esportazione di un documento in Html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Quando esportiamo un documento in html, Aspose.Words creerà anche un foglio di stile CSS per formattare il documento.
// Impostare il flag "ExportEmbeddedCss" su "true" salva il foglio di stile CSS in un file .css,
// e collega il file dal documento html usando un elemento <link>.
// Impostare il flag su "false" incorporerà il foglio di stile CSS all'interno del documento Html,
// il che creerà un solo file invece di due.
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

## Vedi anche

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
