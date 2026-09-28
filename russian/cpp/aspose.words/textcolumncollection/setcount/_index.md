---
title: "Aspose::Words::TextColumnCollection::SetCount method"
linktitle: "SetCount"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::TextColumnCollection::SetCount method. Распределяет текст по указанному количеству колонок в C++."
type: docs
weight: 13000
url: /ru/cpp/aspose.words/textcolumncollection/setcount/
---
## TextColumnCollection::SetCount method


Размещает текст в указанном количестве колонок.

```cpp
void Aspose::Words::TextColumnCollection::SetCount(int32_t newCount)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| newCount | int32_t | Количество колонок, в которые будет распределён текст. |
## Примечания


Когда [EvenlySpaced](../get_evenlyspaced/) установлен в **false** и вы увеличиваете количество колонок, создаются новые объекты [TextColumn](../../textcolumn/) с нулевой шириной и отступом. Необходимо задать ширину и отступ для новых колонок.

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
