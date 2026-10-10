---
title: "Aspose::Words::Document::RemoveBlankPages 方法"
linktitle: "RemoveBlankPages"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::RemoveBlankPages 方法。删除 C++ 文档中的空白页。"
type: docs
weight: 67500
url: /zh/cpp/aspose.words/document/removeblankpages/
---
## Document::RemoveBlankPages method


从文档中删除空白页。

```cpp
System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::Document::RemoveBlankPages()
```


### ReturnValue

已将页码列表视为空白并已删除。

## 示例



展示如何从文档中删除空白页。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Blank pages.docx");
ASSERT_EQ(2, doc->get_PageCount());
doc->RemoveBlankPages();
doc->UpdatePageLayout();
ASSERT_EQ(1, doc->get_PageCount());
```

## 另见

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
