---
title: Aspose::Words::Tables::Table::set_DistanceRight method
linktitle: set_DistanceRight
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::Table::set_DistanceRight method. Sets distance between table right and the surrounding text, in points in C++.'
type: docs
weight: 116000
url: /cpp/aspose.words.tables/table/set_distanceright/
---
## Table::set_DistanceRight method


Sets distance between table right and the surrounding text, in points.

```cpp
void Aspose::Words::Tables::Table::set_DistanceRight(double value)
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

* [get_DistanceRight](../get_distanceright/)

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
