---
title: "Aspose::Words::PageSetup::get_TextColumns метод"
linktitle: "get_TextColumns"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::PageSetup::get_TextColumns метод. Возвращает коллекцию, представляющую набор текстовых колонок в C++."
type: docs
weight: 44000
url: /ru/cpp/aspose.words/pagesetup/get_textcolumns/
---
## PageSetup::get_TextColumns method


Возвращает коллекцию, представляющую набор текстовых колонок.

```cpp
System::SharedPtr<Aspose::Words::TextColumnCollection> Aspose::Words::PageSetup::get_TextColumns()
```


## Примеры



Показывает, как создать несколько равномерно распределенных колонок в разделе.
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

## См. также

* Class [TextColumnCollection](../../textcolumncollection/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
