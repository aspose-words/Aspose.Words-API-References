---
title: "Aspose::Words::Tables::AutoFitBehavior enum"
linktitle: "AutoFitBehavior"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Tables::AutoFitBehavior enum. Определяет, как Aspose.Words изменяет размер таблицы, когда вы вызываете метод AutoFit() в C++."
type: docs
weight: 10000
url: /ru/cpp/aspose.words.tables/autofitbehavior/
---
## AutoFitBehavior enum


Определяет, как Aspose.Words изменяет размер таблицы, когда вы вызываете метод [AutoFit()](../table/autofit/).

```cpp
enum class AutoFitBehavior
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| AutoFitToContents | 0 | Aspose.Words включает опцию AutoFit, удаляет предпочтительную ширину из таблицы и всех ячеек, а затем обновляет макет таблицы. В получившейся таблице ширины ячеек обновляются, чтобы соответствовать содержимому таблицы. Скорее всего, таблица уменьшится. |
| AutoFitToWindow | 1 | Когда вы используете это значение, Aspose.Words включает опцию AutoFit, устанавливает предпочтительную ширину таблицы в 100 %, удаляет предпочтительные ширины из всех ячеек и затем обновляет макет таблицы. В результате таблица занимает всю доступную ширину, а ширины ячеек обновляются, чтобы соответствовать содержимому таблицы. |
| FixedColumnWidths | 2 | Aspose.Words отключает опцию AutoFit и удаляет предпочтительную ширину из таблицы. Ширины ячеек остаются такими, какие указаны в их свойствах [Width](../cellformat/get_width/). |


## Примеры



Показывает, как создать новую таблицу, применяя стиль.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// Мы должны вставить как минимум одну строку перед применением любого форматирования таблицы.
builder->InsertCell();

// Установите стиль таблицы, используемый на основе идентификатора стиля.
// Обратите внимание, что не все стили таблиц доступны при сохранении в формат .doc.
table->set_StyleIdentifier(Aspose::Words::StyleIdentifier::MediumShading1Accent1);

// Частично примените стиль к элементам таблицы на основе предикатов, затем постройте таблицу.
table->set_StyleOptions(Aspose::Words::Tables::TableStyleOptions::FirstColumn | Aspose::Words::Tables::TableStyleOptions::RowBands | Aspose::Words::Tables::TableStyleOptions::FirstRow);
table->AutoFit(Aspose::Words::Tables::AutoFitBehavior::AutoFitToContents);

builder->Writeln(u"Item");
builder->get_CellFormat()->set_RightPadding(40);
builder->InsertCell();
builder->Writeln(u"Quantity (kg)");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Apples");
builder->InsertCell();
builder->Writeln(u"20");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Bananas");
builder->InsertCell();
builder->Writeln(u"40");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Carrots");
builder->InsertCell();
builder->Writeln(u"50");
builder->EndRow();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTableWithStyle.docx");
```


Показывает, как построить отформатированную таблицу 2x2.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->Write(u"Row 1, cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, cell 2.");
builder->EndRow();

// Во время построения таблицы документный построитель применит текущие значения свойств RowFormat/CellFormat.
// к текущей строке/ячейке, в которой находится курсор, и к любым новым строкам/ячейкам при их создании.
ASSERT_EQ(Aspose::Words::Tables::CellVerticalAlignment::Center, table->get_Rows()->idx_get(0)->get_Cells()->idx_get(0)->get_CellFormat()->get_VerticalAlignment());
ASSERT_EQ(Aspose::Words::Tables::CellVerticalAlignment::Center, table->get_Rows()->idx_get(0)->get_Cells()->idx_get(1)->get_CellFormat()->get_VerticalAlignment());

builder->InsertCell();
builder->get_RowFormat()->set_Height(100);
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Exactly);
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Upward);
builder->Write(u"Row 2, cell 1.");
builder->InsertCell();
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
builder->Write(u"Row 2, cell 2.");
builder->EndRow();
builder->EndTable();

// Ранее добавленные строки и ячейки не подвергаются ретроспективному изменению из‑за изменений форматирования построителя.
ASPOSE_ASSERT_EQ(0, table->get_Rows()->idx_get(0)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Auto, table->get_Rows()->idx_get(0)->get_RowFormat()->get_HeightRule());
ASPOSE_ASSERT_EQ(100, table->get_Rows()->idx_get(1)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Exactly, table->get_Rows()->idx_get(1)->get_RowFormat()->get_HeightRule());
ASSERT_EQ(Aspose::Words::TextOrientation::Upward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(0)->get_CellFormat()->get_Orientation());
ASSERT_EQ(Aspose::Words::TextOrientation::Downward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(1)->get_CellFormat()->get_Orientation());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.BuildTable.docx");
```

## См. также

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
