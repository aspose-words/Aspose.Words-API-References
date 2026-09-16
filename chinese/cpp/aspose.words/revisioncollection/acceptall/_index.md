---
title: "Aspose::Words::RevisionCollection::AcceptAll 方法"
linktitle: "AcceptAll"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::RevisionCollection::AcceptAll 方法。接受 C++ 中此集合中的所有修订。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words/revisioncollection/acceptall/
---
## RevisionCollection::AcceptAll method


接受此集合中的所有修订。

```cpp
void Aspose::Words::RevisionCollection::AcceptAll()
```


## 示例



展示如何比较文档。
```cpp
auto docOriginal = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(docOriginal);
builder->Writeln(u"This is the original document.");

auto docEdited = System::MakeObject<Aspose::Words::Document>();
builder = System::MakeObject<Aspose::Words::DocumentBuilder>(docEdited);
builder->Writeln(u"This is the edited document.");

// 比较带有修订的文档将抛出异常。
if (docOriginal->get_Revisions()->get_Count() == 0 && docEdited->get_Revisions()->get_Count() == 0)
{
    docOriginal->Compare(docEdited, u"authorName", System::DateTime::get_Now());
}

// 比较后，原始文档将获得一个新修订
// 针对编辑文档中每个不同的元素。
for (auto&& r : System::IterateOver(docOriginal->get_Revisions()))
{
    std::cout << System::String::Format(u"Revision type: {0}, on a node of type \"{1}\"", r->get_RevisionType(), r->get_ParentNode()->get_NodeType()) << std::endl;
    std::cout << System::String::Format(u"\tChanged text: \"{0}\"", r->get_ParentNode()->GetText()) << std::endl;
}

// 接受这些修订将把原始文档转换为编辑后的文档。
docOriginal->get_Revisions()->AcceptAll();

ASSERT_EQ(docOriginal->GetText(), docEdited->GetText());
```

## 另见

* Class [RevisionCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
