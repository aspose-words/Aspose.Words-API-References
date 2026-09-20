---
title: "Метод Aspose::Words::TableStyle::get_LeftIndent"
linktitle: "get_LeftIndent"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::TableStyle::get_LeftIndent. Получает или задает значение, представляющее левый отступ таблицы в C++."
type: docs
weight: 10000
url: /ru/cpp/aspose.words/tablestyle/get_leftindent/
---
## TableStyle::get_LeftIndent method


Получает или задает значение, представляющее левый отступ таблицы.

```cpp
double Aspose::Words::TableStyle::get_LeftIndent()
```


## Примеры



Показывает, как задать позицию таблицы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ниже представлены два способа горизонтального выравнивания таблицы.
// 1 -  Используйте свойство "Alignment", чтобы выровнять его к позиции на странице, например к центру:
auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
tableStyle->set_Alignment(Aspose::Words::Tables::TableAlignment::Center);
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Blue());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Single);

// Вставьте таблицу и примените к ней стиль, который мы создали.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Aligned to the center of the page");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

table->set_Style(tableStyle);

// 2 -  Используйте "LeftIndent", чтобы указать отступ от левого поля страницы:
tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle2"));
tableStyle->set_LeftIndent(55);
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Green());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Single);

table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Aligned according to left indent");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

table->set_Style(tableStyle);

doc->Save(get_ArtifactsDir() + u"Table.SetTableAlignment.docx");
```

## См. также

* Class [TableStyle](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
