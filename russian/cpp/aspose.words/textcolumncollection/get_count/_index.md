---
title: "Метод Aspose::Words::TextColumnCollection::get_Count"
linktitle: "get_Count"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::TextColumnCollection::get_Count. Получает количество колонок в секции документа в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words/textcolumncollection/get_count/
---
## TextColumnCollection::get_Count method


Возвращает количество колонок в разделе документа.

```cpp
int32_t Aspose::Words::TextColumnCollection::get_Count()
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

* Class [TextColumnCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
