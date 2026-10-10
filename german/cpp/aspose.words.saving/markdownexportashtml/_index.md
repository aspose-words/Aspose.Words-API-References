---
title: "Aspose::Words::Saving::MarkdownExportAsHtml Aufzählung"
linktitle: "MarkdownExportAsHtml"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::MarkdownExportAsHtml Aufzählung. Ermöglicht die Angabe der Elemente, die in C++ als rohes HTML nach Markdown exportiert werden sollen."
type: docs
weight: 66500
url: /de/cpp/aspose.words.saving/markdownexportashtml/
---
## MarkdownExportAsHtml enum


Ermöglicht die Angabe der Elemente, die als rohes HTML nach Markdown exportiert werden sollen.

```cpp
enum class MarkdownExportAsHtml
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Keine | 0 | Exportiert alle Elemente mit Markdown‑Syntax ohne jegliches rohes HTML. |
| Tabellen | 1 | Tabellen als Roh-HTML exportieren. |
| NonCompatibleTables | 2 | Tabellen exportieren, die in reinem Markdown nicht korrekt dargestellt werden können, als Roh-HTML. |


## Beispiele



Zeigt, wie man eine Tabelle nach Markdown als Roh-HTML exportiert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Sample table:");

// Tabelle erstellen.
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

## Siehe auch

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
