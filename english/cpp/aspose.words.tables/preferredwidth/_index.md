---
title: Aspose::Words::Tables::PreferredWidth class
linktitle: PreferredWidth
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::PreferredWidth class. Represents a value and its unit of measure that is used to specify the preferred width of a table or a cell. To learn more, visit the  documentation article in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.tables/preferredwidth/
---
## PreferredWidth class


Represents a value and its unit of measure that is used to specify the preferred width of a table or a cell. To learn more, visit the [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/) documentation article.

```cpp
class PreferredWidth : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| static [Auto](./auto/)() | Returns an instance that represents the "preferred width is not specified" value. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Tables::PreferredWidth\>\&) | Determines whether the specified [PreferredWidth](./) is equal in value to the current [PreferredWidth](./). |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Determines whether the specified object is equal in value to the current object. |
| static [FromPercent](./frompercent/)(double) | A creation method that returns a new instance that represents a preferred width specified as a percentage. |
| static [FromPoints](./frompoints/)(double) | A creation method that returns a new instance that represents a preferred width specified using a number of points. |
| [get_Type](./get_type/)() const | Gets the unit of measure used for this preferred width value. |
| [get_Value](./get_value/)() const | Gets the preferred width value. The unit of measure is specified in the [Type](./get_type/) property. |
| [GetHashCode](./gethashcode/)() const override | Serves as a hash function for this type. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ToString](./tostring/)() const override | Returns a user-friendly string that displays the value of this object. |
| static [Type](./type/)() |  |
## Remarks


Preferred width can be specified as a percentage, number of points or a special "none/auto" value.

The instances of this class are immutable.

## Examples



Shows how to set a table to auto fit to 50% of the width of the page. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Cell #1");
builder->InsertCell();
builder->Write(u"Cell #2");
builder->InsertCell();
builder->Write(u"Cell #3");

table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPercent(50));

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTableWithPreferredWidth.docx");
```


Shows how to set a preferred width for table cells. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// There are two ways of applying the "PreferredWidth" class to table cells.
// 1 -  Set an absolute preferred width based on points:
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(40));
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightYellow());
builder->Writeln(System::String::Format(u"Cell with a width of {0}.", builder->get_CellFormat()->get_PreferredWidth()));

// 2 -  Set a relative preferred width based on percent of the table's width:
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPercent(20));
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightBlue());
builder->Writeln(System::String::Format(u"Cell with a width of {0}.", builder->get_CellFormat()->get_PreferredWidth()));

builder->InsertCell();

// A cell with no preferred width specified will take up the rest of the available space.
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::Auto());

// Each configuration of the "PreferredWidth" property creates a new object.
ASSERT_NE(System::ObjectExt::GetHashCode(table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_PreferredWidth()), System::ObjectExt::GetHashCode(builder->get_CellFormat()->get_PreferredWidth()));

builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightGreen());
builder->Writeln(u"Automatically sized cell.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertCellsWithPreferredWidths.docx");
```

## See Also

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
