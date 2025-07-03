---
title: Aspose::Words::TableStyle::get_ColumnStripe method
linktitle: get_ColumnStripe
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::TableStyle::get_ColumnStripe method. Gets or sets a number of columns to include in the banding when the style specifies odd/even columns banding in C++.'
type: docs
weight: 8000
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
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// We can configure a conditional style of a table to apply a different color to the row/column,
// based on whether the row/column is even or odd, creating an alternating color pattern.
// We can also apply a number n to the row/column banding,
// meaning that the color alternates after every n rows/columns instead of one.
// Create a table where single columns and rows will band the columns will banded in threes.
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

// Apply a line style to all the borders of the table.
auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Black());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Double);

// Set the two colors, which will alternate over every 3 rows.
tableStyle->set_RowStripe(3);
tableStyle->get_ConditionalStyles()->idx_get(Aspose::Words::ConditionalStyleType::OddRowBanding)->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightBlue());
tableStyle->get_ConditionalStyles()->idx_get(Aspose::Words::ConditionalStyleType::EvenRowBanding)->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightCyan());

// Set a color to apply to every even column, which will override any custom row coloring.
tableStyle->set_ColumnStripe(1);
tableStyle->get_ConditionalStyles()->idx_get(Aspose::Words::ConditionalStyleType::EvenColumnBanding)->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightSalmon());

table->set_Style(tableStyle);

// The "StyleOptions" property enables row banding by default.
ASSERT_EQ(Aspose::Words::Tables::TableStyleOptions::FirstRow | Aspose::Words::Tables::TableStyleOptions::FirstColumn | Aspose::Words::Tables::TableStyleOptions::RowBands, table->get_StyleOptions());

// Use the "StyleOptions" property also to enable column banding.
table->set_StyleOptions(table->get_StyleOptions() | Aspose::Words::Tables::TableStyleOptions::ColumnBands);

doc->Save(get_ArtifactsDir() + u"Table.AlternatingRowStyles.docx");
```

## See Also

* Class [TableStyle](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
