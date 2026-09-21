---
title: "Aspose::Words::Saving::MarkdownExportAsHtml enum"
linktitle: "MarkdownExportAsHtml"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::MarkdownExportAsHtml enum. Tillåter att specificera vilka element som ska exporteras till Markdown som rå HTML i C++."
type: docs
weight: 66500
url: /sv/cpp/aspose.words.saving/markdownexportashtml/
---
## MarkdownExportAsHtml enum


Tillåter att ange vilka element som ska exporteras till Markdown som rå HTML.

```cpp
enum class MarkdownExportAsHtml
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| None | 0 | Exportera alla element med Markdown-syntax utan någon rå HTML. |
| Tabeller | 1 | Exportera tabeller som rå HTML. |
| NonCompatibleTables | 2 | Exportera tabeller som inte kan representeras korrekt i ren Markdown som rå HTML. |


## Exempel



Visar hur man exporterar en tabell till Markdown som rå HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Sample table:");

// Skapa tabell.
builder->InsertCell();
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Right);
builder->Write(u"Cell1");
builder->InsertCell();
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->Write(u"Cell2");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_ExportAsHtml(Aspose::Words::Saving::MarkdownExportAsHtml::Tables);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportTableAsHtml.md", saveOptions);
```

## Se även

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
