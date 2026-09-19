---
title: "Metodo Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedSvg"
linktitle: "get_ExportEmbeddedSvg"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedSvg. Specifica se le risorse SVG devono essere incorporate nel documento Html. Il valore predefinito è true in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportembeddedsvg/
---
## HtmlFixedSaveOptions::get_ExportEmbeddedSvg method


Specifica se le risorse SVG devono essere incorporate nel documento Html. Il valore predefinito è **true**.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedSvg() const
```


## Esempi



Mostra come determinare dove memorizzare gli oggetti SVG durante l'esportazione di un documento in Html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

// Quando esportiamo un documento con oggetti SVG in .html,
// Aspose.Words può posizionare questi oggetti in due possibili posizioni.
// Impostare il flag "ExportEmbeddedSvg" su "true" incorporerà tutti i dati grezzi degli oggetti SVG
// all'interno dell'HTML di output, dentro i tag <image>.
// Impostare questo flag su "false" creerà un file nel file system locale per ogni oggetto SVG.
// L'HTML collegherà ogni file usando l'attributo "data" di un tag <object>.
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

## Vedi anche

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
