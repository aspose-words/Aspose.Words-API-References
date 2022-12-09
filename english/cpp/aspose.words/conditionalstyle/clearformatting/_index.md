---
title: ClearFormatting
second_title: Aspose.Words for C++ API Reference
description: Clears formatting of this conditional style.
type: docs
weight: 14
url: /cpp/aspose.words/conditionalstyle/clearformatting/
---
## ConditionalStyle::ClearFormatting method


Clears formatting of this conditional style.

```cpp
void Aspose::Words::ConditionalStyle::ClearFormatting()
```


## Examples



Shows how to reset conditional table styles. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"First row");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Last row");
builder->EndTable();

auto tableStyle = System::DynamicCast<TableStyle>(doc->get_Styles()->Add(StyleType::Table, u"MyTableStyle1"));
table->set_Style(tableStyle);

// Set the table style to color the borders of the first row of the table in red.
tableStyle->get_ConditionalStyles()->get_FirstRow()->get_Borders()->set_Color(System::Drawing::Color::get_Red());

// Set the table style to color the borders of the last row of the table in blue.
tableStyle->get_ConditionalStyles()->get_LastRow()->get_Borders()->set_Color(System::Drawing::Color::get_Blue());

// Below are two ways of using the "ClearFormatting" method to clear the conditional styles.
// 1 -  Clear the conditional styles for a specific part of a table:
tableStyle->get_ConditionalStyles()->idx_get(0)->ClearFormatting();

ASPOSE_ASSERT_EQ(System::Drawing::Color::Empty, tableStyle->get_ConditionalStyles()->get_FirstRow()->get_Borders()->get_Color());

// 2 -  Clear the conditional styles for the entire table:
tableStyle->get_ConditionalStyles()->ClearFormatting();

auto isEmptyColor = [](SharedPtr<ConditionalStyle> s)
{
    return s->get_Borders()->get_Color() == System::Drawing::Color::Empty;
};
ASSERT_TRUE(tableStyle->get_ConditionalStyles()->LINQ_All(isEmptyColor));
```

## See Also

* Class [ConditionalStyle](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
