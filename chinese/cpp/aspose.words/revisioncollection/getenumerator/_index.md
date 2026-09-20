---
title: "Aspose::Words::RevisionCollection::GetEnumerator 方法"
linktitle: "GetEnumerator"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::RevisionCollection::GetEnumerator 方法。返回 C++ 中的枚举器对象。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words/revisioncollection/getenumerator/
---
## RevisionCollection::GetEnumerator method


返回一个枚举器对象。

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Revision>>> Aspose::Words::RevisionCollection::GetEnumerator() override
```


## 示例



展示如何处理文档的修订集合。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");
System::SharedPtr<Aspose::Words::RevisionCollection> revisions = doc->get_Revisions();

// 此集合本身包含一个修订组的集合。
// 每个组都是相邻修订的序列。
std::cout << System::String::Format(u"{0} revision groups:", revisions->get_Groups()->get_Count()) << std::endl;

// 遍历组的集合并打印修订涉及的文本。
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::RevisionGroup>>> e = revisions->get_Groups()->GetEnumerator();
    while (e->MoveNext())
    {
        std::cout << (System::String::Format(u"\tGroup type \"{0}\", ", e->get_Current()->get_RevisionType()) + System::String::Format(u"author: {0}, contents: [{1}]", e->get_Current()->get_Author(), e->get_Current()->get_Text().Trim())) << std::endl;
    }
}

// 每个受修订影响的 Run 都会获得相应的 Revision 对象。
// 修订集合明显大于我们在上面打印的精简形式，
// 这取决于我们在 Microsoft Word 编辑期间将文档分割成了多少个 Run。
std::cout << System::String::Format(u"\n{0} revisions:", revisions->get_Count()) << std::endl;

{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Revision>>> e = revisions->GetEnumerator();
    while (e->MoveNext())
    {
        // StyleDefinitionChange 只影响样式而不影响文档节点。这意味着 "ParentStyle"
        // 属性将始终被使用，而 ParentNode 将始终为 null。
        // 由于所有其他更改都会影响节点，ParentNode 将相应地被使用，而 ParentStyle 将为 null。
        if (e->get_Current()->get_RevisionType() == Aspose::Words::RevisionType::StyleDefinitionChange)
        {
            std::cout << (System::String::Format(u"\tRevision type \"{0}\", ", e->get_Current()->get_RevisionType()) + System::String::Format(u"author: {0}, style: [{1}]", e->get_Current()->get_Author(), e->get_Current()->get_ParentStyle()->get_Name())) << std::endl;
        }
        else
        {
            std::cout << (System::String::Format(u"\tRevision type \"{0}\", ", e->get_Current()->get_RevisionType()) + System::String::Format(u"author: {0}, contents: [{1}]", e->get_Current()->get_Author(), e->get_Current()->get_ParentNode()->GetText().Trim())) << std::endl;
        }
    }
}

// 通过集合拒绝所有修订，将文档恢复到原始形式。
revisions->RejectAll();

ASSERT_EQ(0, revisions->get_Count());
```

## 另见

* Class [Revision](../../revision/)
* Class [RevisionCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
