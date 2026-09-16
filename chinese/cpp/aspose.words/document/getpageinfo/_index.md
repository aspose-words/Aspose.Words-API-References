---
title: "Aspose::Words::Document::GetPageInfo 方法"
linktitle: "GetPageInfo"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::GetPageInfo 方法。获取页面大小、方向以及其他可能对打印或在 C++ 中渲染有用的页面信息。"
type: docs
weight: 62000
url: /zh/cpp/aspose.words/document/getpageinfo/
---
## Document::GetPageInfo method


获取页面尺寸、方向以及可能对打印或渲染有用的其他页面信息。

```cpp
System::SharedPtr<Aspose::Words::Rendering::PageInfo> Aspose::Words::Document::GetPageInfo(int32_t pageIndex)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| pageIndex | int32_t | 基于 0 的页面索引。 |

## 示例



展示如何检查页面是否为彩色。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// 检查文档的首页是否未着色。
ASSERT_FALSE(doc->GetPageInfo(0)->get_Colored());
```

## 另见

* Class [PageInfo](../../../aspose.words.rendering/pageinfo/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
