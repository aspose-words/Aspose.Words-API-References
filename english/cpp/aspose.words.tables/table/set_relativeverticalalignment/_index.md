---
title: Aspose::Words::Tables::Table::set_RelativeVerticalAlignment method
linktitle: set_RelativeVerticalAlignment
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::Table::set_RelativeVerticalAlignment method. Sets floating table relative vertical alignment in C++.'
type: docs
weight: 124000
url: /cpp/aspose.words.tables/table/set_relativeverticalalignment/
---
## Table::set_RelativeVerticalAlignment method


Sets floating table relative vertical alignment.

```cpp
void Aspose::Words::Tables::Table::set_RelativeVerticalAlignment(Aspose::Words::Drawing::VerticalAlignment value)
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
table->set_PreferredWidth(PreferredWidth::FromPoints(300));

// Set the table's location to a place on the page, such as, in this case, the bottom right corner.
table->set_RelativeVerticalAlignment(VerticalAlignment::Bottom);
table->set_RelativeHorizontalAlignment(HorizontalAlignment::Right);

table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Table 2, cell 1");
builder->EndTable();
table->set_PreferredWidth(PreferredWidth::FromPoints(300));

// We can also set a horizontal and vertical offset in points from the paragraph's location where we inserted the table.
table->set_AbsoluteVerticalDistance(50);
table->set_AbsoluteHorizontalDistance(100);

doc->Save(get_ArtifactsDir() + u"Table.ChangeFloatingTableProperties.docx");
```
## See Also

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
