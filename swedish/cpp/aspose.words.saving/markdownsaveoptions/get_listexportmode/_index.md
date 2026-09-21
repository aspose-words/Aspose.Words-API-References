---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_ListExportMode metod"
linktitle: "get_ListExportMode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_ListExportMode metod. Anger hur listobjekt kommer att skrivas till utdatafilen. Standardvärdet är MarkdownSyntax i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.saving/markdownsaveoptions/get_listexportmode/
---
## MarkdownSaveOptions::get_ListExportMode method


Anger hur listobjekt kommer att skrivas till utdatafilen. Standardvärdet är [MarkdownSyntax](../../markdownlistexportmode/).

```cpp
Aspose::Words::Saving::MarkdownListExportMode Aspose::Words::Saving::MarkdownSaveOptions::get_ListExportMode() const
```

## Anmärkningar


När den här egenskapen är inställd på [PlainText](../../markdownlistexportmode/) uppdateras alla listetiketter med hjälp av [UpdateListLabels](../../../aspose.words/document/updatelistlabels/) och exporteras med sina faktiska värden. Sådana listor kan vara inkompatibla med Markdown‑formatet och kommer i så fall att identifieras som vanlig text vid import.

När den här egenskapen är inställd på [MarkdownSyntax](../../markdownlistexportmode/) försöker skribenten att exportera listobjekt på ett sätt som möjliggör automatisk numrering av listor med Markdown.

## Exempel



Visar hur listobjekt kommer att skrivas till markdown-dokumentet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List item.docx");

// Använd MarkdownListExportMode.PlainText eller MarkdownListExportMode.MarkdownSyntax för att exportera listan.
auto options = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
options->set_ListExportMode(markdownListExportMode);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ListExportMode.md", options);
```

## Se även

* Enum [MarkdownListExportMode](../../markdownlistexportmode/)
* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
