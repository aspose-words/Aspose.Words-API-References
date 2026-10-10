---
title: "Aspose::Words::Saving::DocumentSplitCriteria enum"
linktitle: "DocumentSplitCriteria"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::DocumentSplitCriteria enum. Anger hur dokumentet delas upp i delar när det sparas i Html-, Epub- eller Azw3-format i C++."
type: docs
weight: 52000
url: /sv/cpp/aspose.words.saving/documentsplitcriteria/
---
## DocumentSplitCriteria enum


Anger hur dokumentet delas upp i delar när det sparas i [Html](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/) eller [Azw3](../../aspose.words/saveformat/) format.

```cpp
enum class DocumentSplitCriteria
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| None | 0 | Dokumentet delas inte upp. |
| PageBreak | 1 | Dokumentet delas upp i delar vid explicita sidbrytningar. En sidbrytning kan anges med ett [PageBreak](../../aspose.words/controlchar/pagebreak/)‑tecken, ett avsnittsbrytning som anger början på ett nytt avsnitt på en ny sida, eller ett stycke som har sin [PageBreakBefore](../../aspose.words/paragraphformat/get_pagebreakbefore/)‑egenskap satt till **true**. |
| ColumnBreak | 2 | Dokumentet delas upp i delar vid kolumnbrytningar. En kolumnbrytning kan anges med ett [ColumnBreak](../../aspose.words/controlchar/columnbreak/)‑tecken eller ett avsnittsbrytning som anger början på ett nytt avsnitt i en ny kolumn. |
| SectionBreak | 4 | Dokumentet delas upp i delar vid ett avsnittsbrytning av vilken typ som helst. |
| HeadingParagraph | 8 | Dokumentet delas upp i delar vid ett stycke som är formaterat med en rubrikstil **Heading 1**, **Heading 2** osv. Använd tillsammans med [DocumentSplitHeadingLevel](../htmlsaveoptions/get_documentsplitheadinglevel/) för att ange rubriknivåerna (från 1 till den angivna nivån) där uppdelning ska ske. |

## Anmärkningar


[DocumentSplitCriteria](./) is a set of flags which can be combined. For instance you can split the document at page breaks and heading paragraphs in the same export operation.

Olika kriterier kan delvis överlappa. Till exempel får **Heading 1**-stilen ofta egenskapen [PageBreakBefore](../../aspose.words/paragraphformat/get_pagebreakbefore/) så den faller under två kriterier: [PageBreak](./) och [HeadingParagraph](./). Vissa avsnittsbrytningar kan orsaka sidbrytningar och så vidare. I vanliga fall är det mest praktiska att ange bara en flagga.

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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
