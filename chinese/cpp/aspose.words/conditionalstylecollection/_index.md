---
title: "Aspose::Words::ConditionalStyleCollection 类"
linktitle: "ConditionalStyleCollection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ConditionalStyleCollection 类。表示 ConditionalStyle 对象的集合。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 17000
url: /zh/cpp/aspose.words/conditionalstylecollection/
---
## ConditionalStyleCollection class


表示 [ConditionalStyle](../conditionalstyle/) 对象的集合。要了解更多，请访问 [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/) 文档文章。

```cpp
class ConditionalStyleCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::ConditionalStyle>>
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | 清除表样式的所有条件样式。 |
| [get_BottomLeftCell](./get_bottomleftcell/)() | 获取左下单元格样式。 |
| [get_BottomRightCell](./get_bottomrightcell/)() | 获取右下单元格样式。 |
| [get_Count](./get_count/)() const | 获取集合中条件样式的数量。 |
| [get_EvenColumnBanding](./get_evencolumnbanding/)() | 获取偶数列分带样式。 |
| [get_EvenRowBanding](./get_evenrowbanding/)() | 获取偶数行分带样式。 |
| [get_FirstColumn](./get_firstcolumn/)() | 获取第一列样式。 |
| [get_FirstRow](./get_firstrow/)() | 获取第一行样式。 |
| [get_LastColumn](./get_lastcolumn/)() | 获取最后一列样式。 |
| [get_LastRow](./get_lastrow/)() | 获取最后一行样式。 |
| [get_OddColumnBanding](./get_oddcolumnbanding/)() | 获取奇数列分带样式。 |
| [get_OddRowBanding](./get_oddrowbanding/)() | 获取奇数行分带样式。 |
| [get_TopLeftCell](./get_topleftcell/)() | 获取左上单元格样式。 |
| [get_TopRightCell](./get_toprightcell/)() | 获取右上单元格样式。 |
| [GetEnumerator](./getenumerator/)() override | 返回一个枚举器对象，可用于遍历集合中的所有条件样式。 |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(Aspose::Words::ConditionalStyleType) | 通过条件样式类型检索 [ConditionalStyle](../conditionalstyle/) 对象。 |
| [idx_get](./idx_get/)(int32_t) | 通过索引检索 [ConditionalStyle](../conditionalstyle/) 对象。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
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
