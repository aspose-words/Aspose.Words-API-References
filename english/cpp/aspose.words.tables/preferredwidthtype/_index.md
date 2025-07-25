---
title: Aspose::Words::Tables::PreferredWidthType enum
linktitle: PreferredWidthType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::PreferredWidthType enum. Specifies the unit of measurement for the preferred width of a table or cell in C++.'
type: docs
weight: 13000
url: /cpp/aspose.words.tables/preferredwidthtype/
---
## PreferredWidthType enum


Specifies the unit of measurement for the preferred width of a table or cell.

```cpp
enum class PreferredWidthType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Auto | 1 | The preferred width is not specified. The actual width of the table or cell is either specified using the explicit width or will be determined automatically by the table layout algorithm when the table is displayed, depending on the table auto fit setting. |
| Percent | 2 | Measure the current item width using a specified percentage. |
| Points | 3 | Measure the current item width using a specified number of points (1/72 inch). |


## Examples



Shows how to verify the preferred width type and value of a table cell. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
System::SharedPtr<Aspose::Words::Tables::Cell> firstCell = table->get_FirstRow()->get_FirstCell();

ASSERT_EQ(Aspose::Words::Tables::PreferredWidthType::Percent, firstCell->get_CellFormat()->get_PreferredWidth()->get_Type());
ASPOSE_ASSERT_EQ(11.16, firstCell->get_CellFormat()->get_PreferredWidth()->get_Value());
```

## See Also

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
