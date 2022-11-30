---
title: get_ColumnStripe
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a number of columns to include in the banding when the style specifies odd/even columns banding.
type: docs
weight: 79
url: /cpp/aspose.words/tablestyle/get_columnstripe/
---
## TableStyle::get_ColumnStripe method


Gets or sets a number of columns to include in the banding when the style specifies odd/even columns banding.

```cpp
int32_t Aspose::Words::TableStyle::get_ColumnStripe()
```


## Examples



Shows how to create conditional table styles that alternate between rows. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// We can configure a conditional style of a table to apply a different color to the row/column,
// based on whether the row/column is even or odd, creating an alternating color pattern.
// We can also apply a number n to the row/column banding,
// meaning that the color alternates after every n rows/columns instead of one.
// Create a table where single columns and rows will band the columns will banded in threes.
SharedPtr<Table> table = builder->StartTable();
for (int i = 0; i < 15; i++)
{
    for (int j = 0; j < 4; j++)
    {
        builder->InsertCell();
        builder->Writeln(String::Format(u"{0} column.", (j % 2 == 0 ? String(u"Even") : String(u"Odd"))));
        builder->Write(String::Format(u"Row banding {0}.", (i % 3 == 0 ? String(u"start") : String(u"continuation"))));
    }
    builder->EndRow();
}
builder->EndTable();

// Apply a line style to all the borders of the table.
auto tableStyle = System::DynamicCast<TableStyle>(doc->get_Styles()->Add(StyleType::Table, u"MyTableStyle1"));
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Black());
tableStyle->get_Borders()->set_LineStyle(LineStyle::Double);

// Set the two colors, which will alternate over every 3 rows.
tableStyle->set_RowStripe(3);
tableStyle->get_ConditionalStyles()
    ->idx_get(ConditionalStyleType::OddRowBanding)
    ->get_Shading()
    ->set_BackgroundPatternColor(System::Drawing::Color::get_LightBlue());
tableStyle->get_ConditionalStyles()
    ->idx_get(ConditionalStyleType::EvenRowBanding)
    ->get_Shading()
    ->set_BackgroundPatternColor(System::Drawing::Color::get_LightCyan());

// Set a color to apply to every even column, which will override any custom row coloring.
tableStyle->set_ColumnStripe(1);
tableStyle->get_ConditionalStyles()
    ->idx_get(ConditionalStyleType::EvenColumnBanding)
    ->get_Shading()
    ->set_BackgroundPatternColor(System::Drawing::Color::get_LightSalmon());

table->set_Style(tableStyle);

// The "StyleOptions" property enables row banding by default.
ASSERT_EQ(TableStyleOptions::FirstRow | TableStyleOptions::FirstColumn | TableStyleOptions::RowBands, table->get_StyleOptions());

// Use the "StyleOptions" property also to enable column banding.
table->set_StyleOptions(table->get_StyleOptions() | TableStyleOptions::ColumnBands);

doc->Save(ArtifactsDir + u"Table.AlternatingRowStyles.docx");
```

## See Also

* Class [TableStyle](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
