---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportDocumentProperties metod"
linktitle: "get_ExportDocumentProperties"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportDocumentProperties metod. Anger om inbyggda och anpassade dokumentegenskaper ska exporteras till HTML, MHTML eller EPUB. Standardvärdet är false i C++."
type: docs
weight: 14000
url: /sv/cpp/aspose.words.saving/htmlsaveoptions/get_exportdocumentproperties/
---
## HtmlSaveOptions::get_ExportDocumentProperties method


Anger om inbyggda och anpassade dokumentegenskaper ska exporteras till HTML, MHTML eller EPUB. Standardvärdet är **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportDocumentProperties() const
```


## Exempel



Visar hur man använder en specifik kodning när man sparar ett dokument till .epub.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Använd ett SaveOptions-objekt för att ange kodningen för ett dokument som vi ska spara.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Epub);
saveOptions->set_Encoding(System::Text::Encoding::get_UTF8());

// Som standard kommer ett utgående .epub-dokument att ha allt innehåll i en HTML-del.
// Ett delningskriterium låter oss segmentera dokumentet i flera HTML-delar.
// Vi kommer att ange kriterierna för att dela dokumentet i rubrikstycken.
// Detta är användbart för läsare som inte kan läsa HTML-filer som är större än en viss storlek.
saveOptions->set_DocumentSplitCriteria(Aspose::Words::Saving::DocumentSplitCriteria::HeadingParagraph);

// Ange att vi vill exportera dokumentegenskaper.
saveOptions->set_ExportDocumentProperties(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

## Se även

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
