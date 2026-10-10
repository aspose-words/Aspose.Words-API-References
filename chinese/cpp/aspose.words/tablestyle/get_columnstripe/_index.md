---
title: "Aspose::Words::TableStyle::get_ColumnStripe 方法"
linktitle: "get_ColumnStripe"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::TableStyle::get_ColumnStripe 方法。获取或设置在样式指定奇数/偶数列分条时要包含在分条中的列数（C++）。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words/tablestyle/get_columnstripe/
---
## TableStyle::get_ColumnStripe method


获取或设置在样式指定奇偶列分段时要包含在分段中的列数。

```cpp
int32_t Aspose::Words::TableStyle::get_ColumnStripe()
```


## 示例



展示如何创建在行之间交替的条件表格样式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 我们可以配置表格的条件样式，以对行/列应用不同的颜色，
// 基于行/列是偶数还是奇数，创建交替的颜色模式。
// 我们还可以将数字 n 应用于行/列分条，
// 这意味着颜色每 n 行/列交替一次，而不是每一行/列。
// 创建一个表格，使单列和单行的列以三列为一组进行分条。
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
for (int32_t i = 0; i < 15; i++)
{
    for (int32_t j = 0; j < 4; j++)
    {
        builder->InsertCell();
        builder->Writeln(System::String::Format(u"{0} column.", (j % 2 == 0 ? System::String(u"Even") : System::String(u"Odd"))));
        builder->Write(System::String::Format(u"Row banding {0}.", (i % 3 == 0 ? System::String(u"start") : System::String(u"continuation"))));
    }
    builder->EndRow();
}
builder->EndTable();

// 为表格的所有边框应用线条样式。
auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Black());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Double);

// 设置两种颜色，它们将在每 3 行交替显示。
tableStyle->set_RowStripe(3);
tableStyle->get_ConditionalStyles()->idx_get(Aspose::Words::ConditionalStyleType::OddRowBanding)->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightBlue());
tableStyle->get_ConditionalStyles()->idx_get(Aspose::Words::ConditionalStyleType::EvenRowBanding)->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightCyan());

// 设置一种颜色应用于每个偶数列，这将覆盖任何自定义的行着色。
tableStyle->set_ColumnStripe(1);
tableStyle->get_ConditionalStyles()->idx_get(Aspose::Words::ConditionalStyleType::EvenColumnBanding)->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightSalmon());

table->set_Style(tableStyle);

// “StyleOptions”属性默认启用行分条。
ASSERT_EQ(Aspose::Words::Tables::TableStyleOptions::FirstRow | Aspose::Words::Tables::TableStyleOptions::FirstColumn | Aspose::Words::Tables::TableStyleOptions::RowBands, table->get_StyleOptions());

// 同样使用 “StyleOptions” 属性来启用列分条。
table->set_StyleOptions(table->get_StyleOptions() | Aspose::Words::Tables::TableStyleOptions::ColumnBands);

doc->Save(get_ArtifactsDir() + u"Table.AlternatingRowStyles.docx");
```

## 另见

* Class [TableStyle](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
