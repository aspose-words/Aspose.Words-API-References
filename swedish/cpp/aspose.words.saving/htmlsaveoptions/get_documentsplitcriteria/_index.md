---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitCriteria metod"
linktitle: "get_DocumentSplitCriteria"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitCriteria metod. Anger hur dokumentet ska delas upp när det sparas till Html-, Epub- eller Azw3-format. Standard är None för HTML och HeadingParagraph för EPUB och AZW3 i C++."
type: docs
weight: 9000
url: /sv/cpp/aspose.words.saving/htmlsaveoptions/get_documentsplitcriteria/
---
## HtmlSaveOptions::get_DocumentSplitCriteria method


Anger hur dokumentet ska delas upp när det sparas till [Html](../../../aspose.words/saveformat/), [Epub](../../../aspose.words/saveformat/) eller [Azw3](../../../aspose.words/saveformat/) format. Standard är [None](../../documentsplitcriteria/) för HTML och [HeadingParagraph](../../documentsplitcriteria/) för EPUB och AZW3.

```cpp
Aspose::Words::Saving::DocumentSplitCriteria Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitCriteria() const
```

## Anmärkningar


Normalt vill du ha ett dokument sparat till HTML som en enda fil. Men i vissa fall är det att föredra att dela upp resultatet i flera mindre HTML‑sidor. När du sparar i HTML-format kommer dessa sidor att skrivas till enskilda filer eller strömmar. När du sparar i EPUB-format kommer de att införlivas i motsvarande paket.

Ett dokument kan inte delas upp när det sparas i MHTML-format.

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

* Enum [DocumentSplitCriteria](../../documentsplitcriteria/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
