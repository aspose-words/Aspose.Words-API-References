---
title: Aspose::Words::Tables::Table::get_DistanceTop method
linktitle: get_DistanceTop
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::Table::get_DistanceTop method. Gets or sets distance between table top and the surrounding text, in points in C++.'
type: docs
weight: 22000
url: /cpp/aspose.words.tables/table/get_distancetop/
---
## Table::get_DistanceTop method


Gets or sets distance between table top and the surrounding text, in points.

```cpp
double Aspose::Words::Tables::Table::get_DistanceTop()
```


## Examples



Shows how to set distance between table boundaries and text. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table wrapped by text.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
ASPOSE_ASSERT_EQ(25.9, table->get_DistanceTop());
ASPOSE_ASSERT_EQ(25.9, table->get_DistanceBottom());
ASPOSE_ASSERT_EQ(17.3, table->get_DistanceLeft());
ASPOSE_ASSERT_EQ(17.3, table->get_DistanceRight());

// Set distance between table and surrounding text.
table->set_DistanceLeft(24);
table->set_DistanceRight(24);
table->set_DistanceTop(3);
table->set_DistanceBottom(3);

doc->Save(get_ArtifactsDir() + u"Table.DistanceBetweenTableAndText.docx");
```

## See Also

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
