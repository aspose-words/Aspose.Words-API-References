---
title: "Aspose::Words::RevisionGroup::get_RevisionType method"
linktitle: "get_RevisionType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::RevisionGroup::get_RevisionType method. 获取此组中包含的修订类型（C++）。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words/revisiongroup/get_revisiontype/
---
## RevisionGroup::get_RevisionType method


获取此组中包含的修订类型。

```cpp
Aspose::Words::RevisionType Aspose::Words::RevisionGroup::get_RevisionType()
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

* Enum [RevisionType](../../revisiontype/)
* Class [RevisionGroup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
