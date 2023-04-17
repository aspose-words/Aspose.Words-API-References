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

To append [Comment](../) to the document use [InsertAfter()](../) or [InsertBefore()](../) on the paragraph where you want the comment inserted.

After creating a comment, don't forget to set its [Author](../get_author/), [Initial](../get_initial/) and [DateTime](../get_datetime/) properties.

## Examples



Shows how print the contents of all comments and their comment ranges using a document visitor. 
```cpp
void CreateCommentsAndPrintAllInfo()
{
    auto doc = MakeObject<Document>();

    auto newComment = MakeObject<Comment>(doc);
    newComment->set_Author(u"VDeryushev");
    newComment->set_Initial(u"VD");
    newComment->set_DateTime(System::DateTime::get_Now());

    newComment->SetText(u"Comment regarding text.");

    // Add text to the document, warp it in a comment range, and then add your comment.
    SharedPtr<Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
    para->AppendChild(MakeObject<CommentRangeStart>(doc, newComment->get_Id()));
    para->AppendChild(MakeObject<Run>(doc, u"Commented text."));
    para->AppendChild(MakeObject<CommentRangeEnd>(doc, newComment->get_Id()));
    para->AppendChild(newComment);

    // Add two replies to the comment.
    newComment->AddReply(u"John Doe", u"JD", System::DateTime::get_Now(), u"New reply.");
    newComment->AddReply(u"John Doe", u"JD", System::DateTime::get_Now(), u"Another reply.");

    PrintAllCommentInfo(doc->GetChildNodes(NodeType::Comment, true));
}

static void PrintAllCommentInfo(SharedPtr<NodeCollection> comments)
{
    auto commentVisitor = MakeObject<ExComment::CommentInfoPrinter>();

    // Iterate over all top-level comments. Unlike reply-type comments, top-level comments have no ancestor.
    std::function<bool(SharedPtr<Node> c)> haveNoAncestor = [](SharedPtr<Node> c)
    {
        return (System::DynamicCast<Comment>(c))->get_Ancestor() == nullptr;
    };

    for (auto comment : System::IterateOver<Comment>(comments->LINQ_Where(haveNoAncestor)))
    {
        // First, visit the start of the comment range.
        auto commentRangeStart = System::DynamicCast<CommentRangeStart>(comment->get_PreviousSibling()->get_PreviousSibling()->get_PreviousSibling());
        commentRangeStart->Accept(commentVisitor);

        // Then, visit the comment, and any replies that it may have.
        comment->Accept(commentVisitor);

        for (const auto& reply : System::IterateOver<Comment>(comment->get_Replies()))
        {
            reply->Accept(commentVisitor);
        }

        // Finally, visit the end of the comment range, and then print the visitor's text contents.
        auto commentRangeEnd = System::DynamicCast<CommentRangeEnd>(comment->get_PreviousSibling());
        commentRangeEnd->Accept(commentVisitor);

        std::cout << commentVisitor->GetText() << std::endl;
    }
}

class CommentInfoPrinter : public DocumentVisitor
{
public:
    CommentInfoPrinter() : mVisitorIsInsideComment(false), mDocTraversalDepth(0)
    {
        mBuilder = MakeObject<System::Text::StringBuilder>();
        mVisitorIsInsideComment = false;
    }

    String GetText()
    {
        return mBuilder->ToString();
    }

    VisitorAction VisitRun(SharedPtr<Run> run) override
    {
        if (mVisitorIsInsideComment)
        {
            IndentAndAppendLine(String(u"[Run] \"") + run->get_Text() + u"\"");
        }

        return VisitorAction::Continue;
    }

    VisitorAction VisitCommentRangeStart(SharedPtr<CommentRangeStart> commentRangeStart) override
    {
        IndentAndAppendLine(String(u"[Comment range start] ID: ") + commentRangeStart->get_Id());
        mDocTraversalDepth++;
        mVisitorIsInsideComment = true;

        return VisitorAction::Continue;
    }

    VisitorAction VisitCommentRangeEnd(SharedPtr<CommentRangeEnd> commentRangeEnd) override
    {
        mDocTraversalDepth--;
        IndentAndAppendLine(String(u"[Comment range end] ID: ") + commentRangeEnd->get_Id() + u"\n");
        mVisitorIsInsideComment = false;

        return VisitorAction::Continue;
    }

    VisitorAction VisitCommentStart(SharedPtr<Comment> comment) override
    {
        IndentAndAppendLine(
            String::Format(u"[Comment start] For comment range ID {0}, By {1} on {2}", comment->get_Id(), comment->get_Author(), comment->get_DateTime()));
        mDocTraversalDepth++;
        mVisitorIsInsideComment = true;

        return VisitorAction::Continue;
    }

    VisitorAction VisitCommentEnd(SharedPtr<Comment> comment) override
    {
        mDocTraversalDepth--;
        IndentAndAppendLine(u"[Comment end]");
        mVisitorIsInsideComment = false;

        return VisitorAction::Continue;
    }

private:
    bool mVisitorIsInsideComment;
    int mDocTraversalDepth;
    SharedPtr<System::Text::StringBuilder> mBuilder;

    void IndentAndAppendLine(String text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++)
        {
            mBuilder->Append(u"|  ");
        }

        mBuilder->AppendLine(text);
    }
};
```

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
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);
builder->Write(u"Hello world!");

auto comment = MakeObject<Comment>(doc, u"John Doe", u"JD", System::DateTime::get_Today());
builder->get_CurrentParagraph()->AppendChild(comment);
builder->MoveTo(comment->AppendChild(MakeObject<Paragraph>(doc)));
builder->Write(u"Comment text.");

ASSERT_EQ(System::DateTime::get_Today(), comment->get_DateTime());

// In Microsoft Word, we can right-click this comment in the document body to edit it, or reply to it.
doc->Save(ArtifactsDir + u"InlineStory.AddComment.docx");
```

## See Also

* Class [DocumentBase](../../documentbase/)
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
