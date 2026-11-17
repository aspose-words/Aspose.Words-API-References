---
title: Aspose::Words::Comment::Comment constructor
linktitle: Comment
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Comment::Comment constructor. Initializes a new instance of the Comment class in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words/comment/comment/
---
## Comment::Comment(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) constructor


Initializes a new instance of the [Comment](../) class.

```cpp
Aspose::Words::Comment::Comment(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| Parameter | Type | Description |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | The owner document. |
## Remarks


When [Comment](../) is created, it belongs to the specified document, but is not yet part of the document and [ParentNode](../../node/get_parentnode/) is **null**.

To append [Comment](../) to the document use [InsertAfter1()</see> or <see cref="Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertBefore1()](../) on the paragraph where you want the comment inserted.

After creating a comment, don't forget to set its [Author](../get_author/), [Initial](../get_initial/) and [DateTime](../get_datetime/) properties.

## See Also

* Class [DocumentBase](../../documentbase/)
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Comment::Comment(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::String\&, const System::String\&, System::DateTime) constructor


Initializes a new instance of the [Comment](../) class.

```cpp
Aspose::Words::Comment::Comment(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, const System::String &author, const System::String &initial, System::DateTime dateTime)
```


| Parameter | Type | Description |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | The owner document. |
| author | const System::String\& | The author name for the comment. Cannot be **null**. |
| initial | const System::String\& | The author initials for the comment. Cannot be **null**. |
| dateTime | System::DateTime | The date and time for the comment. |

## Examples



Shows how to add a comment to a paragraph. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Hello world!");

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"JD", System::DateTime::get_Today());
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);
builder->MoveTo(comment->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));
builder->Write(u"Comment text.");

ASSERT_EQ(System::DateTime::get_Today(), comment->get_DateTime());

// In Microsoft Word, we can right-click this comment in the document body to edit it, or reply to it.
doc->Save(get_ArtifactsDir() + u"InlineStory.AddComment.docx");
```

## See Also

* Class [DocumentBase](../../documentbase/)
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
