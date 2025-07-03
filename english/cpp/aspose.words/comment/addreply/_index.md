---
title: Aspose::Words::Comment::AddReply method
linktitle: AddReply
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Comment::AddReply method. Adds a reply to this comment in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words/comment/addreply/
---
## Comment::AddReply method


Adds a reply to this comment.

```cpp
System::SharedPtr<Aspose::Words::Comment> Aspose::Words::Comment::AddReply(const System::String &author, const System::String &initial, System::DateTime dateTime, const System::String &text)
```


| Parameter | Type | Description |
| --- | --- | --- |
| author | const System::String\& | The author name for the reply. |
| initial | const System::String\& | The author initials for the reply. |
| dateTime | System::DateTime | The date and time for the reply. |
| text | const System::String\& | The reply text. |

### ReturnValue

The created [Comment](../) node for the reply.
## Remarks


Due to the existing MS Office limitations only 1 level of replies is allowed in the document.

## Examples



Shows how to add a comment to a document, and then reply to it. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");

// Place the comment at a node in the document's body.
// This comment will show up at the location of its paragraph,
// outside the right-side margin of the page, and with a dotted line connecting it to its paragraph.
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// Add a reply, which will show up under its parent comment.
comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"New reply");

// Comments and replies are both Comment nodes.
ASSERT_EQ(2, doc->GetChildNodes(Aspose::Words::NodeType::Comment, true)->get_Count());

// Comments that do not reply to other comments are "top-level". They have no ancestor comments.
ASSERT_TRUE(System::TestTools::IsNull(comment->get_Ancestor()));

// Replies have an ancestor top-level comment.
ASPOSE_ASSERT_EQ(comment, comment->get_Replies()->idx_get(0)->get_Ancestor());

doc->Save(get_ArtifactsDir() + u"Comment.AddCommentWithReply.docx");
```

## See Also

* Class [Comment](../)
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
