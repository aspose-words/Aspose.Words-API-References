---
title: Aspose::Words::ConditionalStyleCollection::get_FirstColumn method
linktitle: get_FirstColumn
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ConditionalStyleCollection::get_FirstColumn method. Gets the first column style in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words/conditionalstylecollection/get_firstcolumn/
---
## ConditionalStyleCollection::get_FirstColumn method


Gets the first column style.

```cpp
System::SharedPtr<Aspose::Words::ConditionalStyle> Aspose::Words::ConditionalStyleCollection::get_FirstColumn()
```


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
auto tableStyle = System::ExplicitCast<TableStyle>(doc->get_Styles()->Add(StyleType::Table, u"MyTableStyle1"));

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

* Class [ConditionalStyle](../../conditionalstyle/)
* Class [ConditionalStyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
