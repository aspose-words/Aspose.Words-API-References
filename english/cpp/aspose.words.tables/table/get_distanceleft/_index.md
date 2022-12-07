---
title: get_DistanceLeft
second_title: Aspose.Words for C++ API Reference
description: Gets distance between table left and the surrounding text, in points.
type: docs
weight: 248
url: /cpp/aspose.words.tables/table/get_distanceleft/
---
## Table::get_DistanceLeft method


Gets distance between table left and the surrounding text, in points.

```cpp
double Aspose::Words::Tables::Table::get_DistanceLeft()
```


## Examples



Shows the minimum distance operations between table boundaries and text. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Table wrapped by text.docx");

SharedPtr<Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

ASPOSE_ASSERT_EQ(25.9, table->get_DistanceTop());
ASPOSE_ASSERT_EQ(25.9, table->get_DistanceBottom());
ASPOSE_ASSERT_EQ(17.3, table->get_DistanceLeft());
ASPOSE_ASSERT_EQ(17.3, table->get_DistanceRight());
```

## See Also

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words](../../../)
