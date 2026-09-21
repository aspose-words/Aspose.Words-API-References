---
title: "Aspose::Words::DocumentBuilderOptions::get_ContextTableFormatting metod"
linktitle: "get_ContextTableFormatting"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBuilderOptions::get_ContextTableFormatting metod. Sant om formateringen som tillämpas på tabellinnehåll inte påverkar formateringen av innehållet som följer efter. Standardvärdet är true i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words/documentbuilderoptions/get_contexttableformatting/
---
## DocumentBuilderOptions::get_ContextTableFormatting method


Standardvärdet är **true**.

```cpp
bool Aspose::Words::DocumentBuilderOptions::get_ContextTableFormatting() const
```


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

* Class [DocumentBuilderOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
