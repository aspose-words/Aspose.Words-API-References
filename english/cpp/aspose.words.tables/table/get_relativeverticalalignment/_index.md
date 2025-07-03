---
title: Aspose::Words::Tables::Table::get_RelativeVerticalAlignment method
linktitle: get_RelativeVerticalAlignment
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::Table::get_RelativeVerticalAlignment method. Gets or sets floating table relative vertical alignment in C++.'
type: docs
weight: 31000
url: /cpp/aspose.words.tables/table/get_relativeverticalalignment/
---
## Table::get_RelativeVerticalAlignment method


Gets or sets floating table relative vertical alignment.

```cpp
Aspose::Words::Drawing::VerticalAlignment Aspose::Words::Tables::Table::get_RelativeVerticalAlignment()
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

* Enum [VerticalAlignment](../../../aspose.words.drawing/verticalalignment/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
