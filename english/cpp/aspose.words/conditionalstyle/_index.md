---
title: ConditionalStyle
second_title: Aspose.Words for C++ API Reference
description: Represents special formatting applied to some area of a table with assigned table style.
type: docs
weight: 196
url: /cpp/aspose.words/conditionalstyle/
---
## ConditionalStyle class


Represents special formatting applied to some area of a table with assigned table style.

```cpp
class ConditionalStyle : public Aspose::Words::IBorderAttrSource, public Aspose::Words::IShadingAttrSource, public Aspose::Words::IParaAttrSource, public Aspose::Words::IRunAttrSource
```

## Methods

| Method | Description |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Clears formatting of this conditional style. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override |  |
| [get_Borders](./get_borders/)() | Gets the collection of default cell borders for the conditional style. |
| [get_BottomPadding](./get_bottompadding/)() | Gets or sets the amount of space (in points) to add below the contents of table cells. |
| [get_Font](./get_font/)() | Gets the character formatting of the conditional style. |
| [get_LeftPadding](./get_leftpadding/)() | Gets or sets the amount of space (in points) to add to the left of the contents of table cells. |
| [get_ParagraphFormat](./get_paragraphformat/)() | Gets the paragraph formatting of the conditional style. |
| [get_RightPadding](./get_rightpadding/)() | Gets or sets the amount of space (in points) to add to the right of the contents of table cells. |
| [get_Shading](./get_shading/)() | Gets a [Shading](../shading/) object that refers to the shading formatting for this conditional style. |
| [get_TopPadding](./get_toppadding/)() | Gets or sets the amount of space (in points) to add above the contents of table cells. |
| [get_Type](./get_type/)() | Gets table area to which this conditional style relates. |
| [GetHashCode](./gethashcode/)() const override | Calculates hash code for this object. |
| [set_BottomPadding](./set_bottompadding/)(double) | Setter for [Aspose::Words::ConditionalStyle::get_BottomPadding](./get_bottompadding/). |
| [set_LeftPadding](./set_leftpadding/)(double) | Setter for [Aspose::Words::ConditionalStyle::get_LeftPadding](./get_leftpadding/). |
| [set_RightPadding](./set_rightpadding/)(double) | Setter for [Aspose::Words::ConditionalStyle::get_RightPadding](./get_rightpadding/). |
| [set_TopPadding](./set_toppadding/)(double) | Setter for [Aspose::Words::ConditionalStyle::get_TopPadding](./get_toppadding/). |

## Examples




Shows how to work with certain area styles of a table. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Table> table = builder->StartTable();
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

// Create a custom table style.
auto tableStyle = System::DynamicCast<TableStyle>(doc->get_Styles()->Add(StyleType::Table, u"MyTableStyle1"));

// Conditional styles are formatting changes that affect only some of the table's cells
// based on a predicate, such as the cells being in the last row.
// Below are three ways of accessing a table style's conditional styles from the "ConditionalStyles" collection.
// 1 -  By style type:
tableStyle->get_ConditionalStyles()
    ->idx_get(ConditionalStyleType::FirstRow)
    ->get_Shading()
    ->set_BackgroundPatternColor(System::Drawing::Color::get_AliceBlue());

// 2 -  By index:
tableStyle->get_ConditionalStyles()->idx_get(0)->get_Borders()->set_Color(System::Drawing::Color::get_Black());
tableStyle->get_ConditionalStyles()->idx_get(0)->get_Borders()->set_LineStyle(LineStyle::DotDash);
ASSERT_EQ(ConditionalStyleType::FirstRow, tableStyle->get_ConditionalStyles()->idx_get(0)->get_Type());

// 3 -  As a property:
tableStyle->get_ConditionalStyles()->get_FirstRow()->get_ParagraphFormat()->set_Alignment(ParagraphAlignment::Center);

// Apply padding and text formatting to conditional styles.
tableStyle->get_ConditionalStyles()->get_LastRow()->set_BottomPadding(10);
tableStyle->get_ConditionalStyles()->get_LastRow()->set_LeftPadding(10);
tableStyle->get_ConditionalStyles()->get_LastRow()->set_RightPadding(10);
tableStyle->get_ConditionalStyles()->get_LastRow()->set_TopPadding(10);
tableStyle->get_ConditionalStyles()->get_LastColumn()->get_Font()->set_Bold(true);

// List all possible style conditions.
{
    SharedPtr<System::Collections::Generic::IEnumerator<SharedPtr<ConditionalStyle>>> enumerator = tableStyle->get_ConditionalStyles()->GetEnumerator();
    while (enumerator->MoveNext())
    {
        SharedPtr<ConditionalStyle> currentStyle = enumerator->get_Current();
        if (currentStyle != nullptr)
        {
            std::cout << System::EnumGetName(currentStyle->get_Type()) << std::endl;
        }
    }
}

// Apply the custom style, which contains all conditional styles, to the table.
table->set_Style(tableStyle);

// Our style applies some conditional styles by default.
ASSERT_EQ(TableStyleOptions::FirstRow | TableStyleOptions::FirstColumn | TableStyleOptions::RowBands, table->get_StyleOptions());

// We will need to enable all other styles ourselves via the "StyleOptions" property.
table->set_StyleOptions(table->get_StyleOptions() | TableStyleOptions::LastRow | TableStyleOptions::LastColumn);

doc->Save(ArtifactsDir + u"Table.ConditionalStyles.docx");
```

