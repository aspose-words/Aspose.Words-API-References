---
title: "Aspose::Words::Framesets::Frameset::get_ChildFramesets 方法"
linktitle: "get_ChildFramesets"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Framesets::Frameset::get_ChildFramesets 方法。获取 C++ 中子框架和框架页面的集合。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.framesets/frameset/get_childframesets/
---
## Frameset::get_ChildFramesets method


获取子框架和框架页面的集合。

```cpp
System::SharedPtr<Aspose::Words::Framesets::FramesetCollection> Aspose::Words::Framesets::Frameset::get_ChildFramesets() const
```


## 示例



展示如何访问页面上的框架。
```cpp
// 文档包含多个带有指向其他文档链接的框架。
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Frameset.docx");

ASSERT_EQ(3, doc->get_Frameset()->get_ChildFramesets()->get_Count());
// 我们可以检查默认 URL（网页 URL 或本地文档）或框架是否为外部资源。
ASSERT_EQ(u"https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx", doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->get_FrameDefaultUrl());
ASSERT_TRUE(doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->get_IsFrameLinkToFile());

ASSERT_EQ(u"Document.docx", doc->get_Frameset()->get_ChildFramesets()->idx_get(1)->get_FrameDefaultUrl());
ASSERT_FALSE(doc->get_Frameset()->get_ChildFramesets()->idx_get(1)->get_IsFrameLinkToFile());

// 更改我们其中一个框架的属性。
doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->set_FrameDefaultUrl(u"https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx");
doc->get_Frameset()->get_ChildFramesets()->idx_get(0)->get_ChildFramesets()->idx_get(0)->set_IsFrameLinkToFile(false);
```

## 另见

* Class [FramesetCollection](../../framesetcollection/)
* Class [Frameset](../)
* Namespace [Aspose::Words::Framesets](../../)
* Library [Aspose.Words for C++](../../../)
