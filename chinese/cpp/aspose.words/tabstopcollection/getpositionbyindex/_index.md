---
title: "Aspose::Words::TabStopCollection::GetPositionByIndex 方法"
linktitle: "GetPositionByIndex"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::TabStopCollection::GetPositionByIndex 方法。获取指定索引处制表位的位置（以点为单位）（C++）。"
type: docs
weight: 10000
url: /zh/cpp/aspose.words/tabstopcollection/getpositionbyindex/
---
## TabStopCollection::GetPositionByIndex method


获取指定索引处制表位的位置（以点为单位）。

```cpp
double Aspose::Words::TabStopCollection::GetPositionByIndex(int32_t index)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| index | int32_t | 制表位集合中的索引。 |

### ReturnValue

制表位的位置。

## 示例



展示如何通过索引查找制表位并验证其位置。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat()->get_TabStops();

tabStops->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(30), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
tabStops->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(60), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

// 验证集合中第二个制表位的位置。
ASSERT_NEAR(Aspose::Words::ConvertUtil::MillimeterToPoint(60), tabStops->GetPositionByIndex(1), 0.1);
```

## 另见

* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
