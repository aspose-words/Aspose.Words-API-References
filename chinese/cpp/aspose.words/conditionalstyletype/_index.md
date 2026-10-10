---
title: "Aspose::Words::ConditionalStyleType 枚举"
linktitle: "ConditionalStyleType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ConditionalStyleType 枚举。表示在 C++ 中表格样式中可以定义条件格式的可能表格区域。"
type: docs
weight: 85000
url: /zh/cpp/aspose.words/conditionalstyletype/
---
## ConditionalStyleType enum


表示在表格样式中可以定义条件格式的可能表格区域。

```cpp
enum class ConditionalStyleType
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| FirstRow | 0 | 指定表格第一行的格式设置。 |
| FirstColumn | 1 | 指定表格第一列的格式。 |
| LastRow | 2 | 指定表格最后一行的格式。 |
| LastColumn | 3 | 指定表格最后一列的格式。 |
| OddRowBanding | 4 | 指定奇数行条纹的格式。 |
| OddColumnBanding | 5 | 指定奇数列条纹的格式。 |
| EvenRowBanding | 6 | 指定偶数行条纹的格式。 |
| EvenColumnBanding | 7 | 指定偶数列条纹的格式。 |
| TopLeftCell | 8 | 指定表格左上单元格的格式。 |
| TopRightCell | 9 | 指定表格右上单元格的格式。 |
| BottomLeftCell | 10 | 指定表格左下单元格的格式。 |
| BottomRightCell | 11 | 指定表格右下单元格的格式。 |


## 示例



展示如何使用表格的特定区域样式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Cell 1");
builder->InsertCell();
builder->Write(u"Cell 2");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Cell 3");
builder->InsertCell();
builder->Write(u"Cell 4");
builder->EndTable();

// 创建自定义表格样式。
auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));

// 条件样式是仅影响表格部分单元格的格式更改
// 基于谓词，例如单元格位于最后一行时。
// 下面展示了从 "ConditionalStyles" 集合中访问表格样式的条件样式的三种方法。
// 1 -  按样式类型：
tableStyle->get_ConditionalStyles()->idx_get(Aspose::Words::ConditionalStyleType::FirstRow)->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_AliceBlue());

// 2 -  按索引：
tableStyle->get_ConditionalStyles()->idx_get(0)->get_Borders()->set_Color(System::Drawing::Color::get_Black());
tableStyle->get_ConditionalStyles()->idx_get(0)->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::DotDash);
ASSERT_EQ(Aspose::Words::ConditionalStyleType::FirstRow, tableStyle->get_ConditionalStyles()->idx_get(0)->get_Type());

// 3 -  作为属性：
tableStyle->get_ConditionalStyles()->get_FirstRow()->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

// 对条件样式应用填充和文本格式。
tableStyle->get_ConditionalStyles()->get_LastRow()->set_BottomPadding(10);
tableStyle->get_ConditionalStyles()->get_LastRow()->set_LeftPadding(10);
tableStyle->get_ConditionalStyles()->get_LastRow()->set_RightPadding(10);
tableStyle->get_ConditionalStyles()->get_LastRow()->set_TopPadding(10);
tableStyle->get_ConditionalStyles()->get_LastColumn()->get_Font()->set_Bold(true);

// 列出所有可能的样式条件。
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::ConditionalStyle>>> enumerator = tableStyle->get_ConditionalStyles()->GetEnumerator();
    while (enumerator->MoveNext())
    {
        System::SharedPtr<Aspose::Words::ConditionalStyle> currentStyle = enumerator->get_Current();
        if (currentStyle != nullptr)
        {
            std::cout << System::EnumGetName(currentStyle->get_Type()) << std::endl;
        }
    }
}

// 将包含所有条件样式的自定义样式应用于表格。
table->set_Style(tableStyle);

// 我们的样式默认应用了一些条件样式。
ASSERT_EQ(Aspose::Words::Tables::TableStyleOptions::FirstRow | Aspose::Words::Tables::TableStyleOptions::FirstColumn | Aspose::Words::Tables::TableStyleOptions::RowBands, table->get_StyleOptions());

// 我们需要通过 "StyleOptions" 属性自行启用所有其他样式。
table->set_StyleOptions(table->get_StyleOptions() | Aspose::Words::Tables::TableStyleOptions::LastRow | Aspose::Words::Tables::TableStyleOptions::LastColumn);

doc->Save(get_ArtifactsDir() + u"Table.ConditionalStyles.docx");
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
