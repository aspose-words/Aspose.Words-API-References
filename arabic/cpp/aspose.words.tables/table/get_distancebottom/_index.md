---
title: "Aspose::Words::Tables::Table::get_DistanceBottom طريقة"
linktitle: "get_DistanceBottom"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Tables::Table::get_DistanceBottom طريقة. يحصل على أو يضبط المسافة بين أسفل الجدول والنص المحيط، بالنقاط في C++."
type: docs
weight: 19000
url: /ar/cpp/aspose.words.tables/table/get_distancebottom/
---
## Table::get_DistanceBottom method


يحصل أو يضبط المسافة بين أسفل الجدول والنص المحيط، بالنقاط.

```cpp
double Aspose::Words::Tables::Table::get_DistanceBottom()
```


## أمثلة



يظهر كيفية ضبط المسافة بين حدود الجدول والنص.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table wrapped by text.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
ASPOSE_ASSERT_EQ(25.9, table->get_DistanceTop());
ASPOSE_ASSERT_EQ(25.9, table->get_DistanceBottom());
ASPOSE_ASSERT_EQ(17.3, table->get_DistanceLeft());
ASPOSE_ASSERT_EQ(17.3, table->get_DistanceRight());

// ضبط المسافة بين الجدول والنص المحيط.
table->set_DistanceLeft(24);
table->set_DistanceRight(24);
table->set_DistanceTop(3);
table->set_DistanceBottom(3);

doc->Save(get_ArtifactsDir() + u"Table.DistanceBetweenTableAndText.docx");
```

## انظر أيضًا

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
