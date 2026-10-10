---
title: "Aspose::Words::RevisionGroupCollection::get_Count 方法"
linktitle: "get_Count"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::RevisionGroupCollection::get_Count 方法。返回集合中修订组的数量（C++）。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words/revisiongroupcollection/get_count/
---
## RevisionGroupCollection::get_Count method


返回集合中修订组的数量。

```cpp
int32_t Aspose::Words::RevisionGroupCollection::get_Count()
```


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

* Class [RevisionGroupCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
