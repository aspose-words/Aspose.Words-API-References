---
title: "Aspose::Words::TextColumnCollection::get_Count metod"
linktitle: "get_Count"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::TextColumnCollection::get_Count metod. Hämtar antalet kolumner i sektionen av ett dokument i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words/textcolumncollection/get_count/
---
## TextColumnCollection::get_Count method


Hämtar antalet kolumner i avsnittet i ett dokument.

```cpp
int32_t Aspose::Words::TextColumnCollection::get_Count()
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
