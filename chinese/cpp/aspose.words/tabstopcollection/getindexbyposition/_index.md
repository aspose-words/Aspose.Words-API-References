---
title: "Aspose::Words::TabStopCollection::GetIndexByPosition 方法"
linktitle: "GetIndexByPosition"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::TabStopCollection::GetIndexByPosition 方法。获取在 C++ 中指定位置（以点为单位）的制表位的索引。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words/tabstopcollection/getindexbyposition/
---
## TabStopCollection::GetIndexByPosition method


获取具有指定点位置的制表位的索引。

```cpp
int32_t Aspose::Words::TabStopCollection::GetIndexByPosition(double position)
```


## 示例



展示如何查找位置以判断是否存在制表位并获取其索引。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat()->get_TabStops();

// 在 30mm 位置添加制表位。
tabStops->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(30), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

// 由 "GetIndexByPosition" 返回的结果为 "0"，确认存在制表位
// 在 30mm 处存在于此集合中，且索引为 0。
ASSERT_EQ(0, tabStops->GetIndexByPosition(Aspose::Words::ConvertUtil::MillimeterToPoint(30)));

// 由 "GetIndexByPosition" 返回的 "-1" 确认
// 此集合中没有位置为 60mm 的制表位。
ASSERT_EQ(-1, tabStops->GetIndexByPosition(Aspose::Words::ConvertUtil::MillimeterToPoint(60)));
```

## 另见

* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
