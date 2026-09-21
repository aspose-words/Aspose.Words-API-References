---
title: "Aspose::Words::PageSetup::get_TextColumns‑metod"
linktitle: "get_TextColumns"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::PageSetup::get_TextColumns‑metod. Returnerar en samling som representerar uppsättningen av textkolumner i C++."
type: docs
weight: 44000
url: /sv/cpp/aspose.words/pagesetup/get_textcolumns/
---
## PageSetup::get_TextColumns method


Returnerar en samling som representerar uppsättningen av textkolumner.

```cpp
System::SharedPtr<Aspose::Words::TextColumnCollection> Aspose::Words::PageSetup::get_TextColumns()
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

* Class [TextColumnCollection](../../textcolumncollection/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
