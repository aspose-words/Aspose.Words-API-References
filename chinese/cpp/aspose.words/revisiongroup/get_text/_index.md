---
title: "Aspose::Words::RevisionGroup::get_Text 方法"
linktitle: "get_Text"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::RevisionGroup::get_Text 方法。返回在 C++ 中插入/删除/移动的文本或格式更改的描述。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words/revisiongroup/get_text/
---
## RevisionGroup::get_Text method


返回插入/删除/移动的文本或格式更改的描述。

```cpp
System::String Aspose::Words::RevisionGroup::get_Text()
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

* Class [RevisionGroup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
