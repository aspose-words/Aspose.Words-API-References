---
title: Accept
second_title: Aspose.Words for C++ API Reference
description: Accepts a visitor.
type: docs
weight: 14
url: /cpp/aspose.words/commentrangeend/accept/
---
## CommentRangeEnd.Accept method


Accepts a visitor.

```cpp
bool Aspose::Words::CommentRangeEnd::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parameter | Type | Description |
| --- | --- | --- |
| visitor | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | The visitor that will visit the node. |

### ReturnValue


False if the visitor requested the enumeration to stop.

Calls [VisitCommentRangeEnd()](../../documentvisitor/visitcommentrangeend/).

For more info see the Visitor design pattern.

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

