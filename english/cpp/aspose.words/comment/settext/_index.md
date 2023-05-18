---
title: Aspose::Words::Comment::SetText method
linktitle: SetText
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Comment::SetText method. This is a convenience method that allows to easily set text of the comment in C++.'
type: docs
weight: 22000
url: /cpp/aspose.words/comment/settext/
---
## Comment::SetText method


This is a convenience method that allows to easily set text of the comment.

```cpp
void Aspose::Words::Comment::SetText(const System::String &text)
```


| Parameter | Type | Description |
| --- | --- | --- |
| text | const System::String\& | The new text of the comment. |
## Remarks


This method allows to quickly set text of a comment from a string. The string can contain paragraph breaks, this will create paragraphs of text in the comment accordingly. If you want to insert more complex elements into the comment, for example bookmarks or tables or apply rich formatting, then you need to use the appropriate node classes to build up the comment text.

## Examples



Shows how to add a comment to a document, and then reply to it. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

auto comment = MakeObject<Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");

// Place the comment at a node in the document's body.
// This comment will show up at the location of its paragraph,
// outside the right-side margin of the page, and with a dotted line connecting it to its paragraph.
builder->get_CurrentParagraph()->AppendChild(comment);

// Add a reply, which will show up under its parent comment.
comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"New reply");

// Comments and replies are both Comment nodes.
ASSERT_EQ(2, doc->GetChildNodes(NodeType::Comment, true)->get_Count());

// Comments that do not reply to other comments are "top-level". They have no ancestor comments.
ASSERT_TRUE(comment->get_Ancestor() == nullptr);

// Replies have an ancestor top-level comment.
ASPOSE_ASSERT_EQ(comment, comment->get_Replies()->idx_get(0)->get_Ancestor());

doc->Save(ArtifactsDir + u"Comment.AddCommentWithReply.docx");
```

## See Also

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
