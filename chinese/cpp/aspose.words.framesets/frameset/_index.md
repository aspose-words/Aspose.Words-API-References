---
title: "Aspose::Words::Framesets::Frameset class"
linktitle: "Frameset"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Framesets::Frameset 类。表示一个框架页面或框架页面上的单个框架。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 1000
url: /zh/cpp/aspose.words.framesets/frameset/
---
## Frameset class


表示帧页面或帧页面上的单个帧。要了解更多，请访问 [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/) 文档文章。

```cpp
class Frameset : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Frameset](./frameset/)() |  |
| [get_ChildFramesets](./get_childframesets/)() const | 获取子框架和框架页面的集合。 |
| [get_FrameDefaultUrl](./get_framedefaulturl/)() | 获取或设置要在此框架中显示的网页 URL 或文档文件名。 |
| [get_IsFrameLinkToFile](./get_isframelinktofile/)() | 获取或设置一个值，指示在 [FrameDefaultUrl](./get_framedefaulturl/) 属性中指定的网页或文档文件名是否为框架链接的外部资源。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FrameDefaultUrl](./set_framedefaulturl/)(const System::String\&) | 用于设置 [Aspose::Words::Framesets::Frameset::get_FrameDefaultUrl](./get_framedefaulturl/) 的 setter。 |
| [set_IsFrameLinkToFile](./set_isframelinktofile/)(bool) | 用于设置 [Aspose::Words::Framesets::Frameset::get_IsFrameLinkToFile](./get_isframelinktofile/) 的 setter。 |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Framesets](../)
* Library [Aspose.Words for C++](../../)
