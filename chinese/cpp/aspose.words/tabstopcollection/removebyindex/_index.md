---
title: "Aspose::Words::TabStopCollection::RemoveByIndex 方法"
linktitle: "RemoveByIndex"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::TabStopCollection::RemoveByIndex 方法。删除集合中指定索引处的制表位（C++）。"
type: docs
weight: 14000
url: /zh/cpp/aspose.words/tabstopcollection/removebyindex/
---
## TabStopCollection::RemoveByIndex method


从集合中移除指定索引处的制表位。

```cpp
void Aspose::Words::TabStopCollection::RemoveByIndex(int32_t index)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| index | int32_t | 制表位集合中的索引。 |

## 示例



展示如何通过索引选择文档中的制表位并将其删除。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat()->get_TabStops();

tabStops->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(30), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
tabStops->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(60), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

ASSERT_EQ(2, tabStops->get_Count());

// 删除第一个制表位。
tabStops->RemoveByIndex(0);

ASSERT_EQ(1, tabStops->get_Count());

doc->Save(get_ArtifactsDir() + u"TabStopCollection.RemoveByIndex.docx");
```

## 另见

* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
