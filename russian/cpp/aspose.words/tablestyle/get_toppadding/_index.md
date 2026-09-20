---
title: "Aspose::Words::TableStyle::get_TopPadding метод"
linktitle: "get_TopPadding"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::TableStyle::get_TopPadding метод. Получает или задает количество пространства (в пунктах), добавляемого над содержимым ячеек таблицы в C++."
type: docs
weight: 15000
url: /ru/cpp/aspose.words/tablestyle/get_toppadding/
---
## TableStyle::get_TopPadding method


Получает или задает количество пространства (в пунктах), добавляемого над содержимым ячеек таблицы.

```cpp
double Aspose::Words::TableStyle::get_TopPadding()
```


## Примеры



Показывает, как создать пользовательские настройки стиля для таблицы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Name");
builder->InsertCell();
builder->Write(u"مرحبًا");
builder->EndRow();
builder->InsertCell();
builder->InsertCell();
builder->EndTable();

auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
tableStyle->set_AllowBreakAcrossPages(true);
tableStyle->set_CellSpacing(5);
tableStyle->set_BottomPadding(20);
tableStyle->set_LeftPadding(5);
tableStyle->set_RightPadding(10);
tableStyle->set_TopPadding(20);
tableStyle->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_AntiqueWhite());
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Blue());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::DotDash);
tableStyle->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);

table->set_Style(tableStyle);

// Установка свойств стиля таблицы может влиять на свойства самой таблицы.
ASSERT_FALSE(table->get_Bidi());
ASPOSE_ASSERT_EQ(5.0, table->get_CellSpacing());
ASSERT_EQ(u"MyTableStyle1", table->get_StyleName());

doc->Save(get_ArtifactsDir() + u"Table.TableStyleCreation.docx");
```

## См. также

* Class [TableStyle](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
