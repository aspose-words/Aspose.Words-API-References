---
title: "Aspose::Words::Rendering::PageInfo::get_Colored 方法"
linktitle: "get_Colored"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Rendering::PageInfo::get_Colored 方法。若页面包含彩色内容，则返回 true，使用 C++。"
type: docs
weight: 1500
url: /zh/cpp/aspose.words.rendering/pageinfo/get_colored/
---
## PageInfo::get_Colored method


如果页面包含彩色内容，则返回 **true**。

```cpp
bool Aspose::Words::Rendering::PageInfo::get_Colored()
```


## 示例



展示如何检查页面是否为彩色。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// 检查文档的首页是否未着色。
ASSERT_FALSE(doc->GetPageInfo(0)->get_Colored());
```

## 另见

* Class [PageInfo](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
