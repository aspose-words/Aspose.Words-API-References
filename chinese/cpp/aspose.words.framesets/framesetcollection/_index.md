---
title: "Aspose::Words::Framesets::FramesetCollection class"
linktitle: "FramesetCollection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Framesets::FramesetCollection 类。表示 Frameset 类实例的集合。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.framesets/framesetcollection/
---
## FramesetCollection class


表示 [Frameset](../frameset/) 类实例的集合。要了解更多信息，请访问 [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/) 文档文章。

```cpp
class FramesetCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Framesets::Frameset>>
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [FramesetCollection](./framesetcollection/)() |  |
| [get_Count](./get_count/)() | 获取集合中包含的框架或框架页面的数量。 |
| [GetEnumerator](./getenumerator/)() override | 返回一个遍历集合的枚举器。 |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | 获取指定索引处的帧或帧页面。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| 类型定义 | 描述 |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |

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
