---
title: "Aspose::Words::Saving::MarkdownExportAsHtml enum"
linktitle: "MarkdownExportAsHtml"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::MarkdownExportAsHtml enum. Consente di specificare gli elementi da esportare in Markdown come HTML grezzo in C++."
type: docs
weight: 66500
url: /it/cpp/aspose.words.saving/markdownexportashtml/
---
## MarkdownExportAsHtml enum


Consente di specificare gli elementi da esportare in Markdown come HTML grezzo.

```cpp
enum class MarkdownExportAsHtml
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | 0 | Esporta tutti gli elementi usando la sintassi Markdown senza alcun HTML grezzo. |
| Tabelle | 1 | Esporta le tabelle come HTML grezzo. |
| NonCompatibleTables | 2 | Esporta le tabelle che non possono essere rappresentate correttamente in Markdown puro come HTML grezzo. |


## Esempi



Mostra come esportare una tabella in Markdown come HTML grezzo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Sample table:");

// Crea tabella.
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

## Vedi anche

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
