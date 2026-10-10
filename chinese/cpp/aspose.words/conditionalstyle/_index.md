---
title: "Aspose::Words::ConditionalStyle 类"
linktitle: "ConditionalStyle"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ConditionalStyle 类。表示应用于具有指定表格样式的表格某些区域的特殊格式。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 16000
url: /zh/cpp/aspose.words/conditionalstyle/
---
## ConditionalStyle class


表示应用于具有指定表格样式的表格某个区域的特殊格式。要了解更多信息，请访问 [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/) 文档文章。

```cpp
class ConditionalStyle : public Aspose::Words::IBorderAttrSource,
                         public Aspose::Words::IShadingAttrSource,
                         public Aspose::Words::IParaAttrSource,
                         public Aspose::Words::IRunAttrSource
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | 清除此条件样式的格式。 |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | 将此条件样式与指定的对象进行比较。 |
| [get_Borders](./get_borders/)() | 获取此条件样式的默认单元格边框集合。 |
| [get_BottomPadding](./get_bottompadding/)() | 获取或设置在表格单元格内容下方添加的空间量（以点为单位）。 |
| [get_Font](./get_font/)() | 获取此条件样式的字符格式。 |
| [get_LeftPadding](./get_leftpadding/)() | 获取或设置在表格单元格内容左侧添加的空间量（以点为单位）。 |
| [get_ParagraphFormat](./get_paragraphformat/)() | 获取此条件样式的段落格式。 |
| [get_RightPadding](./get_rightpadding/)() | 获取或设置在表格单元格内容右侧添加的空间量（以点为单位）。 |
| [get_Shading](./get_shading/)() | 获取一个指向此条件样式的阴影格式的 [Shading](../shading/) 对象。 |
| [get_TopPadding](./get_toppadding/)() | 获取或设置在表格单元格内容上方添加的空间量（以点为单位）。 |
| [get_Type](./get_type/)() | 获取此条件样式关联的表格区域。 |
| [GetHashCode](./gethashcode/)() const override | 计算此对象的哈希码。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BottomPadding](./set_bottompadding/)(double) | 用于 [Aspose::Words::ConditionalStyle::get_BottomPadding](./get_bottompadding/) 的设置器。 |
| [set_LeftPadding](./set_leftpadding/)(double) | 用于 [Aspose::Words::ConditionalStyle::get_LeftPadding](./get_leftpadding/) 的设置器。 |
| [set_RightPadding](./set_rightpadding/)(double) | 用于 [Aspose::Words::ConditionalStyle::get_RightPadding](./get_rightpadding/) 的设置器。 |
| [set_TopPadding](./set_toppadding/)(double) | 用于 [Aspose::Words::ConditionalStyle::get_TopPadding](./get_toppadding/) 的设置器。 |
| static [Type](./type/)() |  |

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
