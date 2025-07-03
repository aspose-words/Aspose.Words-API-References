---
title: Aspose::Words::ParagraphCollection class
linktitle: ParagraphCollection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ParagraphCollection class. Provides typed access to a collection of Paragraph nodes. To learn more, visit the  documentation article in C++.'
type: docs
weight: 48000
url: /cpp/aspose.words/paragraphcollection/
---
## ParagraphCollection class


Provides typed access to a collection of [Paragraph](../paragraph/) nodes. To learn more, visit the [Working with Paragraphs](https://docs.aspose.com/words/cpp/working-with-paragraphs/) documentation article.

```cpp
class ParagraphCollection : public Aspose::Words::NodeCollection
```

## Methods

| Method | Description |
| --- | --- |
| [Add](../nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Adds a node to the end of the collection. |
| [Clear](../nodecollection/clear/)() | Removes all nodes from this collection and from the document. |
| [Contains](../nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Determines whether a node is in the collection. |
| [get_Count](../nodecollection/get_count/)() | Gets the number of nodes in the collection. |
| [GetEnumerator](../nodecollection/getenumerator/)() override | Provides a simple "foreach" style iteration over the collection of nodes. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Retrieves a [Paragraph](../paragraph/) at the given index. |
| [IndexOf](../nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Returns the zero-based index of the specified node. |
| [Insert](../nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Inserts a node into the collection at the specified index. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Removes the node from the collection and from the document. |
| [RemoveAt](../nodecollection/removeat/)(int32_t) | Removes the node at the specified index from the collection and from the document. |
| [ToArray](./toarray/)() | Copies all paragraphs from the collection to a new array of paragraphs. |
| static [Type](./type/)() |  |

## Examples



Shows how to check whether a paragraph is a move revision. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

// This document contains "Move" revisions, which appear when we highlight text with the cursor,
// and then drag it to move it to another location
// while tracking revisions in Microsoft Word via "Review" -> "Track changes".
ASSERT_EQ(6, doc->get_Revisions()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Revision>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Revision> r)>>([](System::SharedPtr<Aspose::Words::Revision> r) -> bool
{
    return r->get_RevisionType() == Aspose::Words::RevisionType::Moving;
}))));

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

// Move revisions consist of pairs of "Move from", and "Move to" revisions.
// These revisions are potential changes to the document that we can either accept or reject.
// Before we accept/reject a move revision, the document
// must keep track of both the departure and arrival destinations of the text.
// The second and the fourth paragraph define one such revision, and thus both have the same contents.
ASSERT_EQ(paragraphs->idx_get(1)->GetText(), paragraphs->idx_get(3)->GetText());

// The "Move from" revision is the paragraph where we dragged the text from.
// If we accept the revision, this paragraph will disappear,
// and the other will remain and no longer be a revision.
ASSERT_TRUE(paragraphs->idx_get(1)->get_IsMoveFromRevision());

// The "Move to" revision is the paragraph where we dragged the text to.
// If we reject the revision, this paragraph instead will disappear, and the other will remain.
ASSERT_TRUE(paragraphs->idx_get(3)->get_IsMoveToRevision());
```

## See Also

* Class [NodeCollection](../nodecollection/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
