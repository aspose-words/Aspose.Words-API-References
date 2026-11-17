---
title: Aspose::Words::CommentCollection class
linktitle: CommentCollection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::CommentCollection class. Provides typed access to a collection of Comment nodes. To learn more, visit the  documentation article in C++.'
type: docs
weight: 12000
url: /cpp/aspose.words/commentcollection/
---
## CommentCollection class


Provides typed access to a collection of [Comment](../comment/) nodes. To learn more, visit the [Working with Comments](https://docs.aspose.com/words/cpp/working-with-comments/) documentation article.

```cpp
class CommentCollection : public Aspose::Words::NodeCollection
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
| [idx_get](./idx_get/)(int32_t) | Retrieves a [Comment](../comment/) at the given index. |
| [IndexOf](../nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Returns the zero-based index of the specified node. |
| [Insert](../nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Inserts a node into the collection at the specified index. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Removes the node from the collection and from the document. |
| [RemoveAt](../nodecollection/removeat/)(int32_t) | Removes the node at the specified index from the collection and from the document. |
| [ToArray](../nodecollection/toarray/)() | Copies all nodes from the collection to a new array of nodes. |
| static [Type](./type/)() |  |

## Examples



Shows how to mark a comment as "done". 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Helo world!");

// Insert a comment to point out an error.
auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"Fix the spelling error!");
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// Comments have a "Done" flag, which is set to "false" by default.
// If a comment suggests that we make a change within the document,
// we can apply the change, and then also set the "Done" flag afterwards to indicate the correction.
ASSERT_FALSE(comment->get_Done());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->set_Text(u"Hello world!");
comment->set_Done(true);

// Comments that are "done" will differentiate themselves
// from ones that are not "done" with a faded text color.
comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"Add text to this paragraph.");
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

doc->Save(get_ArtifactsDir() + u"Comment.Done.docx");
```

## See Also

* Class [NodeCollection](../nodecollection/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
