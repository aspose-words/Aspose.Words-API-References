---
title: "Aspose::Words::RevisionGroupCollection 类"
linktitle: "RevisionGroupCollection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::RevisionGroupCollection 类。一个包含 RevisionGroup 对象的集合，这些对象表示文档中的修订组。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 55000
url: /zh/cpp/aspose.words/revisiongroupcollection/
---
## RevisionGroupCollection class


一个包含 [RevisionGroup](../revisiongroup/) 对象的集合，这些对象表示文档中的修订组。欲了解更多，请访问 [Track Changes in a Document](https://docs.aspose.com/words/cpp/track-changes-in-a-document/) 文档文章。

```cpp
class RevisionGroupCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::RevisionGroup>>
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
| [get_Count](./get_count/)() | 返回集合中修订组的数量。 |
| [GetEnumerator](./getenumerator/)() override | 返回一个枚举器对象。 |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | 返回指定索引处的修订组。 |
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
## 备注


您不能直接创建此类的实例。请使用 [Groups](../revisioncollection/get_groups/) 属性获取文档中存在的修订组。

## 示例



展示如何打印文档中修订组的信息。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

ASSERT_EQ(7, doc->get_Revisions()->get_Groups()->get_Count());

for (auto&& group : doc->get_Revisions()->get_Groups())
{
    std::cout << System::String::Format(u"Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group->get_Author(), group->get_RevisionType(), group->get_Text()) << std::endl;
}
```


展示如何在文档中获取一组修订。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

System::SharedPtr<Aspose::Words::RevisionGroup> revisionGroup = doc->get_Revisions()->get_Groups()->idx_get(0);
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
