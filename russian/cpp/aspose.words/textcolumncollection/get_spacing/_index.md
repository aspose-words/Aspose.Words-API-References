---
title: "Aspose::Words::TextColumnCollection::get_Spacing method"
linktitle: "get_Spacing"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::TextColumnCollection::get_Spacing method. Когда колонки равномерно распределены, получает или задаёт величину пространства между каждой колонкой в пунктах в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words/textcolumncollection/get_spacing/
---
## TextColumnCollection::get_Spacing method


Когда колонки равномерно распределены, получает или задает величину промежутка между каждой колонкой в пунктах.

```cpp
double Aspose::Words::TextColumnCollection::get_Spacing()
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
