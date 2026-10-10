---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedImages metodo"
linktitle: "get_ExportEmbeddedImages"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedImages metodo. Specifica se le immagini devono essere incorporate nel documento Html in formato Base64. Nota: impostare questa opzione può aumentare significativamente le dimensioni del file Html di output in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportembeddedimages/
---
## HtmlFixedSaveOptions::get_ExportEmbeddedImages method


Specifica se le immagini devono essere incorporate nel documento Html in formato Base64. Nota: impostare questa opzione può aumentare significativamente le dimensioni del file Html di output.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedImages() const
```


## Esempi



Mostra come determinare dove memorizzare le immagini durante l'esportazione di un documento in Html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

// Quando esportiamo un documento con immagini incorporate in .html,
// Aspose.Words può posizionare le immagini in due possibili posizioni.
// Impostare il flag "ExportEmbeddedImages" su "true" memorizzerà i dati grezzi
// per tutte le immagini all'interno del documento HTML di output, nell'attributo "src" dei tag <image>.
// Impostare questo flag su "false" creerà un file immagine nel file system locale per ogni immagine,
// e memorizzerà tutti questi file in una cartella separata.
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportEmbeddedImages(exportImages);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedImages.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedImages.html");

if (exportImages)
{
    ASSERT_FALSE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg"));
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"<img class=\"awimg\" style=\"left:0pt; top:0pt; width:493.1pt; height:300.55pt;\" src=\".+\" />")->get_Success());
}
else
{
    ASSERT_TRUE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg"));
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"<img class=\"awimg\" style=\"left:0pt; top:0pt; width:493.1pt; height:300.55pt;\" ") + u"src=\"HtmlFixedSaveOptions[.]ExportEmbeddedImages/image001[.]jpeg\" />")->get_Success());
}
```

## Vedi anche

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
