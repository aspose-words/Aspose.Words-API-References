---
title: Aspose::Words::Tables::PreferredWidth::ToString method
linktitle: ToString
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::PreferredWidth::ToString method. Returns a user-friendly string that displays the value of this object in C++.'
type: docs
weight: 11000
url: /cpp/aspose.words.tables/preferredwidth/tostring/
---
## PreferredWidth::ToString method


Returns a user-friendly string that displays the value of this object.

```cpp
System::String Aspose::Words::Tables::PreferredWidth::ToString() const override
```


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

* Class [PreferredWidth](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
