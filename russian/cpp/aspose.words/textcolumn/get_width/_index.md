---
title: "Метод Aspose::Words::TextColumn::get_Width"
linktitle: "get_Width"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::TextColumn::get_Width. Получает или задаёт ширину текстовой колонки в пунктах в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words/textcolumn/get_width/
---
## TextColumn::get_Width method


Получает или задает ширину текстовой колонки в пунктах.

```cpp
double Aspose::Words::TextColumn::get_Width()
```


## Примеры



Показывает, как создать колонки с неравномерным интервалом.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();

System::SharedPtr<Aspose::Words::TextColumnCollection> columns = pageSetup->get_TextColumns();
columns->set_EvenlySpaced(false);
columns->SetCount(2);

// Определите количество места, доступного для размещения колонок.
double contentWidth = pageSetup->get_PageWidth() - pageSetup->get_LeftMargin() - pageSetup->get_RightMargin();

ASSERT_NEAR(470.30, contentWidth, 0.01);

// Установите первую колонку узкой.
System::SharedPtr<Aspose::Words::TextColumn> column = columns->idx_get(0);
column->set_Width(100);
column->set_SpaceAfter(20);

// Установите вторую колонку так, чтобы она занимала оставшееся доступное пространство в пределах полей страницы.
column = columns->idx_get(1);
column->set_Width(contentWidth - column->get_Width() - column->get_SpaceAfter());

builder->Writeln(u"Narrow column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Wide column 2.");

doc->Save(get_ArtifactsDir() + u"PageSetup.CustomColumnWidth.docx");
```

## См. также

* Class [TextColumn](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
