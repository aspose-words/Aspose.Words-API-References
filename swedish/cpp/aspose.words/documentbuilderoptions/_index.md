---
title: "Aspose::Words::DocumentBuilderOptions klass"
linktitle: "DocumentBuilderOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBuilderOptions klass. Tillåter att specificera ytterligare alternativ för dokumentbyggprocessen i C++."
type: docs
weight: 22500
url: /sv/cpp/aspose.words/documentbuilderoptions/
---
## DocumentBuilderOptions class


Tillåter att ange ytterligare alternativ för dokumentbyggnadsprocessen.

```cpp
class DocumentBuilderOptions : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [DocumentBuilderOptions](./documentbuilderoptions/)() |  |
| [get_ContextTableFormatting](./get_contexttableformatting/)() const | Standardvärdet är **true**. |
| [get_DesignMode](./get_designmode/)() const | Motsvarar Designläge i Microsoft Word. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ContextTableFormatting](./set_contexttableformatting/)(bool) | Sättare för [Aspose::Words::DocumentBuilderOptions::get_ContextTableFormatting](./get_contexttableformatting/). |
| [set_DesignMode](./set_designmode/)(bool) | Motsvarar Designläge i Microsoft Word. |
| static [Type](./type/)() |  |

## Exempel



Visar hur man ignorerar tabellformatering för innehåll som följer.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builderOptions = System::MakeObject<Aspose::Words::DocumentBuilderOptions>();
builderOptions->set_ContextTableFormatting(true);
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc, builderOptions);

// Lägger till innehåll före tabellen.
// Standardteckenstorlek är 12.
builder->Writeln(u"Font size 12 here.");
builder->StartTable();
builder->InsertCell();
// Ändrar teckenstorleken i tabellen.
builder->get_Font()->set_Size(5);
builder->Write(u"Font size 5 here");
builder->InsertCell();
builder->Write(u"Font size 5 here");
builder->EndRow();
builder->EndTable();

// Om ContextTableFormatting är true, så tillämpas inte tabellformatering på innehållet som följer.
// Om ContextTableFormatting är false, så tillämpas tabellformatering på innehållet som följer.
builder->Writeln(u"Font size 12 here.");

doc->Save(get_ArtifactsDir() + u"Table.ContextTableFormatting.docx");
```

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
