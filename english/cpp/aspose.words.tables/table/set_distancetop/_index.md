---
title: Aspose::Words::Tables::Table::set_DistanceTop method
linktitle: set_DistanceTop
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::Table::set_DistanceTop method. Sets distance between table top and the surrounding text, in points in C++.'
type: docs
weight: 117000
url: /cpp/aspose.words.tables/table/set_distancetop/
---
## Table::set_DistanceTop method


Sets distance between table top and the surrounding text, in points.

```cpp
void Aspose::Words::Tables::Table::set_DistanceTop(double value)
```

## Examples


Shows how to set distance between table boundaries and text.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Table wrapped by text.docx"));

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
ASPOSE_ASSERT_EQ(table->get_DistanceTop(), 25.9);
ASPOSE_ASSERT_EQ(table->get_DistanceBottom(), 25.9);
ASPOSE_ASSERT_EQ(table->get_DistanceLeft(), 17.3);
ASPOSE_ASSERT_EQ(table->get_DistanceRight(), 17.3);

// Set distance between table and surrounding text.
table->set_DistanceLeft(24);
table->set_DistanceRight(24);
table->set_DistanceTop(3);
table->set_DistanceBottom(3);

doc->Save(get_ArtifactsDir() + u"Table.DistanceBetweenTableAndText.docx");
```
## See Also

* [get_DistanceTop](../get_distancetop/)

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
