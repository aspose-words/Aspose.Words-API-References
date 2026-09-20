---
title: "Aspose::Words::RevisionGroup 类"
linktitle: "RevisionGroup"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::RevisionGroup 类。表示一组连续的 Revision 对象。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 54000
url: /zh/cpp/aspose.words/revisiongroup/
---
## RevisionGroup class


表示一组顺序的 [Revision](../revision/) 对象。要了解更多，请访问 [Track Changes in a Document](https://docs.aspose.com/words/cpp/track-changes-in-a-document/) 文档文章。

```cpp
class RevisionGroup : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Author](./get_author/)() | 获取此修订组的作者。 |
| [get_RevisionType](./get_revisiontype/)() | 获取此组中包含的修订类型。 |
| [get_Text](./get_text/)() | 返回插入/删除/移动的文本或格式更改的描述。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
