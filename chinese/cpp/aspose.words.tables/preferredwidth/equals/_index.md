---
title: "Aspose::Words::Tables::PreferredWidth::Equals method"
linktitle: "Equals"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::PreferredWidth::Equals 方法。确定指定的 PreferredWidth 在值上是否等于当前的 PreferredWidth（在 C++ 中）。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.tables/preferredwidth/equals/
---
## PreferredWidth::Equals(const System::SharedPtr\<Aspose::Words::Tables::PreferredWidth\>\&) method


确定指定的 [PreferredWidth](../) 在值上是否等于当前的 [PreferredWidth](../)。

```cpp
bool Aspose::Words::Tables::PreferredWidth::Equals(const System::SharedPtr<Aspose::Words::Tables::PreferredWidth> &other)
```


## 示例



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

* Class [PreferredWidth](../)
* Class [PreferredWidth](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
## PreferredWidth::Equals(System::SharedPtr\<System::Object\>) method


确定指定的对象在值上是否等于当前对象。

```cpp
bool Aspose::Words::Tables::PreferredWidth::Equals(System::SharedPtr<System::Object> obj) override
```


## 示例



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

* Class [PreferredWidth](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
