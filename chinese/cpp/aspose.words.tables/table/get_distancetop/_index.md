---
title: "Aspose::Words::Tables::Table::get_DistanceTop 方法"
linktitle: "get_DistanceTop"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::Table::get_DistanceTop 方法。获取或设置表格顶部与周围文本之间的距离，单位为 C++ 中的点。"
type: docs
weight: 22000
url: /zh/cpp/aspose.words.tables/table/get_distancetop/
---
## Table::get_DistanceTop method


获取或设置表格顶部与周围文本之间的距离（以磅为单位）。

```cpp
double Aspose::Words::Tables::Table::get_DistanceTop()
```


## 示例



展示如何设置表格边界与文本之间的距离。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table wrapped by text.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
ASPOSE_ASSERT_EQ(25.9, table->get_DistanceTop());
ASPOSE_ASSERT_EQ(25.9, table->get_DistanceBottom());
ASPOSE_ASSERT_EQ(17.3, table->get_DistanceLeft());
ASPOSE_ASSERT_EQ(17.3, table->get_DistanceRight());

// 设置表格与周围文本之间的距离。
table->set_DistanceLeft(24);
table->set_DistanceRight(24);
table->set_DistanceTop(3);
table->set_DistanceBottom(3);

doc->Save(get_ArtifactsDir() + u"Table.DistanceBetweenTableAndText.docx");
```

## 另见

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
