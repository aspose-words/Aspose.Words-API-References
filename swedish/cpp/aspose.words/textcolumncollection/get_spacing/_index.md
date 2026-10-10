---
title: "Aspose::Words::TextColumnCollection::get_Spacing metod"
linktitle: "get_Spacing"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::TextColumnCollection::get_Spacing metod. När kolumner är jämnt fördelade hämtas eller sätts mängden utrymme mellan varje kolumn i punkter i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words/textcolumncollection/get_spacing/
---
## TextColumnCollection::get_Spacing method


När kolumnerna är jämnt fördelade, hämtas eller sätts mängden utrymme mellan varje kolumn i punkter.

```cpp
double Aspose::Words::TextColumnCollection::get_Spacing()
```


## Exempel



Visar hur man skapar flera jämnt fördelade kolumner i ett avsnitt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::TextColumnCollection> columns = builder->get_PageSetup()->get_TextColumns();
columns->set_Spacing(100);
columns->SetCount(2);

builder->Writeln(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 2.");

doc->Save(get_ArtifactsDir() + u"PageSetup.ColumnsSameWidth.docx");
```

## Se även

* Class [TextColumnCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
