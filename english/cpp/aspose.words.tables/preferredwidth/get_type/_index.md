---
title: get_Type
second_title: Aspose.Words for C++ API Reference
description: Gets the unit of measure used for this preferred width value.
type: docs
weight: 53
url: /cpp/aspose.words.tables/preferredwidth/get_type/
---
## PreferredWidth::get_Type method


Gets the unit of measure used for this preferred width value.

```cpp
Aspose::Words::Tables::PreferredWidthType Aspose::Words::Tables::PreferredWidth::get_Type() const
```


## Examples



Shows how to verify the preferred width type and value of a table cell. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Tables.docx");

SharedPtr<Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
SharedPtr<Cell> firstCell = table->get_FirstRow()->get_FirstCell();

ASSERT_EQ(PreferredWidthType::Percent, firstCell->get_CellFormat()->get_PreferredWidth()->get_Type());
ASPOSE_ASSERT_EQ(11.16, firstCell->get_CellFormat()->get_PreferredWidth()->get_Value());
```

## See Also

* Enum [PreferredWidthType](../../preferredwidthtype/)
* Class [PreferredWidth](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words](../../../)
