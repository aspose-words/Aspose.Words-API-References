---
title: PreferredWidthType
second_title: Aspose.Words for C++ API Reference
description: Specifies the unit of measurement for the preferred width of a table or cell.
type: docs
weight: 157
url: /cpp/aspose.words.tables/preferredwidthtype/
---
## PreferredWidthType enum


Specifies the unit of measurement for the preferred width of a table or cell.

### Values

| Name | Value | Description |
| --- | --- | --- |
| Auto | 1 | The preferred width is not specified. The actual width of the table or cell is either specified using the explicit width or will be determined automatically by the table layout algorithm when the table is displayed, depending on the table auto fit setting. |
| Percent | 2 | Measure the current item width using a specified percentage. |
| Points | 3 | Measure the current item width using a specified number of points (1/72 inch). |


## Examples




Shows how to verify the preferred width type and value of a table cell. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Tables.docx");

SharedPtr<Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
SharedPtr<Cell> firstCell = table->get_FirstRow()->get_FirstCell();

ASSERT_EQ(PreferredWidthType::Percent, firstCell->get_CellFormat()->get_PreferredWidth()->get_Type());
ASPOSE_ASSERT_EQ(11.16, firstCell->get_CellFormat()->get_PreferredWidth()->get_Value());
```

