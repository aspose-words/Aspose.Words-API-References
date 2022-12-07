---
title: get_RelativeHorizontalAlignment
second_title: Aspose.Words for C++ API Reference
description: Gets or sets floating table relative horizontal alignment.
type: docs
weight: 378
url: /cpp/aspose.words.tables/table/get_relativehorizontalalignment/
---
## Table::get_RelativeHorizontalAlignment method


Gets or sets floating table relative horizontal alignment.

```cpp
Aspose::Words::Drawing::HorizontalAlignment Aspose::Words::Tables::Table::get_RelativeHorizontalAlignment()
```


## Examples



Shows how set the location of floating tables. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Table> table = builder->StartTable();
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

doc->Save(ArtifactsDir + u"Table.ChangeFloatingTableProperties.docx");
```

## See Also

* Enum [HorizontalAlignment](../../../aspose.words.drawing/horizontalalignment/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words](../../../)
