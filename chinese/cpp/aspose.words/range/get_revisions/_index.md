---
title: "Aspose::Words::Range::get_Revisions method"
linktitle: "get_Revisions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Range::get_Revisions method. 获取此范围内存在的修订（已跟踪的更改）集合（C++）。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words/range/get_revisions/
---
## Range::get_Revisions method


获取此范围内存在的修订（已跟踪更改）集合。

```cpp
System::SharedPtr<Aspose::Words::RevisionCollection> Aspose::Words::Range::get_Revisions()
```

## 备注


返回的集合是一个 “live” 集合，这意味着如果删除包含修订的文档部分，已删除的修订将自动从该集合中消失。

## 示例



展示如何在范围内使用修订。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
for (auto&& revision : System::IterateOver(paragraph->get_Range()->get_Revisions()))
{
    if (revision->get_RevisionType() == Aspose::Words::RevisionType::Deletion)
    {
        revision->Accept();
    }
}

// 拒绝第一节的修订。
doc->get_FirstSection()->get_Range()->get_Revisions()->RejectAll();
```

## 另见

* Class [RevisionCollection](../../revisioncollection/)
* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
