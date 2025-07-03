---
title: Aspose::Words::Tables::Table::get_AbsoluteHorizontalDistance method
linktitle: get_AbsoluteHorizontalDistance
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::Table::get_AbsoluteHorizontalDistance method. Gets or sets absolute horizontal floating table position specified by the table properties, in points. Default value is 0 in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words.tables/table/get_absolutehorizontaldistance/
---
## Table::get_AbsoluteHorizontalDistance method


Gets or sets absolute horizontal floating table position specified by the table properties, in points. Default value is 0.

```cpp
double Aspose::Words::Tables::Table::get_AbsoluteHorizontalDistance()
```


## Examples



Shows how set the location of floating tables. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Table 1, cell 1");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

// Set the table's location to a place on the page, such as, in this case, the bottom right corner.
table->set_RelativeVerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Bottom);
table->set_RelativeHorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Right);

table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Table 2, cell 1");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

// We can also set a horizontal and vertical offset in points from the paragraph's location where we inserted the table.
table->set_AbsoluteVerticalDistance(50);
table->set_AbsoluteHorizontalDistance(100);

doc->Save(get_ArtifactsDir() + u"Table.ChangeFloatingTableProperties.docx");
```

## See Also

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
