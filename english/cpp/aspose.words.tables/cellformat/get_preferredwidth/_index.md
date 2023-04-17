---
title: Aspose::Words::Tables::CellFormat::get_PreferredWidth method
linktitle: get_PreferredWidth
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::CellFormat::get_PreferredWidth method. Returns or sets the preferred width of the cell in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words.tables/cellformat/get_preferredwidth/
---
## CellFormat::get_PreferredWidth method


Returns or sets the preferred width of the cell.

```cpp
System::SharedPtr<Aspose::Words::Tables::PreferredWidth> Aspose::Words::Tables::CellFormat::get_PreferredWidth()
```

## Remarks


The preferred width (along with the table's Auto Fit option) determines how the actual width of the cell is calculated by the table layout algorithm. [Table](../../table/) layout can be performed by Aspose.Words when it saves the document or by Microsoft Word when it displays the document.

The preferred width can be specified in points or in percent. The preferred width can also be specified as "auto", which means no preferred width is specified.

The default value is [Auto](../../preferredwidth/auto/).

## Examples



Shows how to set a preferred width for table cells. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);
SharedPtr<Table> table = builder->StartTable();

// There are two ways of applying the "PreferredWidth" class to table cells.
// 1 -  Set an absolute preferred width based on points:
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(PreferredWidth::FromPoints(40));
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightYellow());
builder->Writeln(String::Format(u"Cell with a width of {0}.", builder->get_CellFormat()->get_PreferredWidth()));

// 2 -  Set a relative preferred width based on percent of the table's width:
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(PreferredWidth::FromPercent(20));
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightBlue());
builder->Writeln(String::Format(u"Cell with a width of {0}.", builder->get_CellFormat()->get_PreferredWidth()));

builder->InsertCell();

// A cell with no preferred width specified will take up the rest of the available space.
builder->get_CellFormat()->set_PreferredWidth(PreferredWidth::Auto());

// Each configuration of the "PreferredWidth" property creates a new object.
ASSERT_NE(System::ObjectExt::GetHashCode(table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_PreferredWidth()),
          System::ObjectExt::GetHashCode(builder->get_CellFormat()->get_PreferredWidth()));

builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightGreen());
builder->Writeln(u"Automatically sized cell.");

doc->Save(ArtifactsDir + u"DocumentBuilder.InsertCellsWithPreferredWidths.docx");
```

## See Also

* Class [PreferredWidth](../../preferredwidth/)
* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
