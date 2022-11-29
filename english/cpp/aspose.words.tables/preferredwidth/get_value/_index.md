---
title: get_Value
second_title: Aspose.Words for C++ API Reference
description: Gets the preferred width value. The unit of measure is specified in the Type property.
type: docs
weight: 66
url: /cpp/aspose.words.tables/preferredwidth/get_value/
---
## PreferredWidth::get_Value method


Gets the preferred width value. The unit of measure is specified in the [Type](../get_type/) property.

```cpp
double Aspose::Words::Tables::PreferredWidth::get_Value() const
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

* Class [PreferredWidth](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words](../../../)
