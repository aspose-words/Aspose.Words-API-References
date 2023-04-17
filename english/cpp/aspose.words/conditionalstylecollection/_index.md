---
title: Aspose::Words::ConditionalStyleCollection class
linktitle: ConditionalStyleCollection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ConditionalStyleCollection class. Represents a collection of ConditionalStyle objects. To learn more, visit the  documentation article in C++.'
type: docs
weight: 17000
url: /cpp/aspose.words/conditionalstylecollection/
---
## ConditionalStyleCollection class


Represents a collection of [ConditionalStyle](../conditionalstyle/) objects. To learn more, visit the [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/) documentation article.

```cpp
class ConditionalStyleCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::ConditionalStyle>>
```

## Methods

| Method | Description |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Clears all conditional styles of the table style. |
| [get_BottomLeftCell](./get_bottomleftcell/)() | Gets the bottom left cell style. |
| [get_BottomRightCell](./get_bottomrightcell/)() | Gets the bottom right cell style. |
| [get_Count](./get_count/)() const | Gets the number of conditional styles in the collection. |
| [get_EvenColumnBanding](./get_evencolumnbanding/)() | Gets the even column banding style. |
| [get_EvenRowBanding](./get_evenrowbanding/)() | Gets the even row banding style. |
| [get_FirstColumn](./get_firstcolumn/)() | Gets the first column style. |
| [get_FirstRow](./get_firstrow/)() | Gets the first row style. |
| [get_LastColumn](./get_lastcolumn/)() | Gets the last column style. |
| [get_LastRow](./get_lastrow/)() | Gets the last row style. |
| [get_OddColumnBanding](./get_oddcolumnbanding/)() | Gets the odd column banding style. |
| [get_OddRowBanding](./get_oddrowbanding/)() | Gets the odd row banding style. |
| [get_TopLeftCell](./get_topleftcell/)() | Gets the top left cell style. |
| [get_TopRightCell](./get_toprightcell/)() | Gets the top right cell style. |
| [GetEnumerator](./getenumerator/)() override | Returns an enumerator object that can be used to iterate over all conditional styles in the collection. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(Aspose::Words::ConditionalStyleType) | Retrieves a [ConditionalStyle](../conditionalstyle/) object by conditional style type. |
| [idx_get](./idx_get/)(int32_t) | Retrieves a [ConditionalStyle](../conditionalstyle/) object by index. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
