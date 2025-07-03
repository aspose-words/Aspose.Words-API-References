---
title: Aspose::Words::Range::get_Revisions method
linktitle: get_Revisions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Range::get_Revisions method. Gets a collection of revisions (tracked changes) that exist in this range in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words/range/get_revisions/
---
## Range::get_Revisions method


Gets a collection of revisions (tracked changes) that exist in this range.

```cpp
System::SharedPtr<Aspose::Words::RevisionCollection> Aspose::Words::Range::get_Revisions()
```

## Remarks


The returned collection is a "live" collection, which means if you remove parts of a document that contain revisions, the deleted revisions will automatically disappear from this collection.

## Examples



Shows how to work with revisions in range. 
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

// Reject the first section revisions.
doc->get_FirstSection()->get_Range()->get_Revisions()->RejectAll();
```

## See Also

* Class [RevisionCollection](../../revisioncollection/)
* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
