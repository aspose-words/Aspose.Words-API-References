---
title: "Metodo Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedFonts"
linktitle: "get_ExportEmbeddedFonts"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedFonts. Specifica se i font devono essere incorporati nel documento Html in formato Base64. Nota: impostare questo flag può aumentare significativamente le dimensioni del file Html di output in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportembeddedfonts/
---
## HtmlFixedSaveOptions::get_ExportEmbeddedFonts method


Specifica se i caratteri devono essere incorporati nel documento Html in formato Base64. Nota: impostare questa opzione può aumentare significativamente le dimensioni del file Html di output.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedFonts() const
```


## Esempi



Mostra come determinare dove memorizzare i font incorporati durante l'esportazione di un documento in Html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

// Quando esportiamo un documento con font incorporati in .html,
// Aspose.Words può posizionare i font in due possibili posizioni.
// Impostare il flag "ExportEmbeddedFonts" su "true" memorizzerà i dati grezzi dei font incorporati all'interno del foglio di stile CSS,
// nella proprietà "url" della regola "@font-face". Questo può creare un enorme file di foglio di stile CSS
// e ridurre il numero di file esterni che questa conversione HTML creerà.
// Impostare questa opzione su "false" creerà un file per ogni carattere.
// Il foglio di stile CSS collegherà ogni file di carattere usando la proprietà "url" della regola "@font-face".
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

## Vedi anche

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
