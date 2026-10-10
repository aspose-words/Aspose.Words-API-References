---
title: "Aspose::Words::ConditionalStyle::ClearFormatting 方法"
linktitle: "ClearFormatting"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ConditionalStyle::ClearFormatting 方法。清除此条件样式在 C++ 中的格式设置。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words/conditionalstyle/clearformatting/
---
## ConditionalStyle::ClearFormatting method


清除此条件样式的格式。

```cpp
void Aspose::Words::ConditionalStyle::ClearFormatting()
```


## 示例



展示如何重置条件表格样式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"First row");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Last row");
builder->EndTable();

auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
table->set_Style(tableStyle);

// 将表格样式设置为将表格第一行的边框着色为红色。
tableStyle->get_ConditionalStyles()->get_FirstRow()->get_Borders()->set_Color(System::Drawing::Color::get_Red());

// 将表格样式设置为将表格最后一行的边框着色为蓝色。
tableStyle->get_ConditionalStyles()->get_LastRow()->get_Borders()->set_Color(System::Drawing::Color::get_Blue());

// 以下是使用 "ClearFormatting" 方法清除条件样式的两种方式。
// 1 - 清除表格特定部分的条件样式：
tableStyle->get_ConditionalStyles()->idx_get(0)->ClearFormatting();

ASPOSE_ASSERT_EQ(System::Drawing::Color::Empty, tableStyle->get_ConditionalStyles()->get_FirstRow()->get_Borders()->get_Color());

// 2 - 清除整个表格的条件样式：
tableStyle->get_ConditionalStyles()->ClearFormatting();

ASSERT_TRUE(tableStyle->get_ConditionalStyles()->LINQ_All(static_cast<System::Func<System::SharedPtr<Aspose::Words::ConditionalStyle>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::ConditionalStyle> s)>>([](System::SharedPtr<Aspose::Words::ConditionalStyle> s) -> bool
{
    return s->get_Borders()->get_Color() == System::Drawing::Color::Empty;
}))));
```

## 另见

* Class [ConditionalStyle](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
