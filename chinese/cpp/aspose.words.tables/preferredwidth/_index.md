---
title: "Aspose::Words::Tables::PreferredWidth 类"
linktitle: "PreferredWidth"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::PreferredWidth 类。表示用于指定表格或单元格首选宽度的数值及其计量单位。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.tables/preferredwidth/
---
## PreferredWidth class


表示用于指定表格或单元格首选宽度的数值及其计量单位。要了解更多信息，请访问 [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/) 文档文章。

```cpp
class PreferredWidth : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| static [Auto](./auto/)() | 返回一个表示"未指定首选宽度"值的实例。 |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Tables::PreferredWidth\>\&) | 确定指定的 [PreferredWidth](./) 在数值上是否等于当前的 [PreferredWidth](./)。 |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | 确定指定的对象在值上是否等于当前对象。 |
| static [FromPercent](./frompercent/)(double) | 一种创建方法，返回表示以百分比指定的首选宽度的新实例。 |
| static [FromPoints](./frompoints/)(double) | 一种创建方法，返回表示使用点数指定的首选宽度的新实例。 |
| [get_Type](./get_type/)() const | 获取此首选宽度值使用的计量单位。 |
| [get_Value](./get_value/)() const | 获取首选宽度值。计量单位在 [Type](./get_type/) 属性中指定。 |
| [GetHashCode](./gethashcode/)() const override | 作为此类型的哈希函数。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ToString](./tostring/)() const override | 返回一个用户友好的字符串，显示此对象的值。 |
| static [Type](./type/)() |  |
## 备注


首选宽度可以指定为百分比、点数或特殊的"none/auto"值。

此类的实例是不可变的。

## 示例



展示如何将表格自动适配为页面宽度的 50%。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Cell #1");
builder->InsertCell();
builder->Write(u"Cell #2");
builder->InsertCell();
builder->Write(u"Cell #3");

table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPercent(50));

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTableWithPreferredWidth.docx");
```


展示如何为表格单元格设置首选宽度。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// 有两种方式将 "PreferredWidth" 类应用于表格单元格。
// 1 - 基于点数设置绝对首选宽度：
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(40));
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightYellow());
builder->Writeln(System::String::Format(u"Cell with a width of {0}.", builder->get_CellFormat()->get_PreferredWidth()));

// 2 - 基于表格宽度的百分比设置相对首选宽度：
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPercent(20));
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightBlue());
builder->Writeln(System::String::Format(u"Cell with a width of {0}.", builder->get_CellFormat()->get_PreferredWidth()));

builder->InsertCell();

// 未指定首选宽度的单元格将占用剩余的可用空间。
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::Auto());

// 每次对 "PreferredWidth" 属性的配置都会创建一个新对象。
ASSERT_NE(System::ObjectExt::GetHashCode(table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_PreferredWidth()), System::ObjectExt::GetHashCode(builder->get_CellFormat()->get_PreferredWidth()));

builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightGreen());
builder->Writeln(u"Automatically sized cell.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertCellsWithPreferredWidths.docx");
```

## 另见

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
