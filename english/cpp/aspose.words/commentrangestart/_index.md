---
title: Aspose::Words::CommentRangeStart class
linktitle: CommentRangeStart
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::CommentRangeStart class. Denotes the start of a region of text that has a comment associated with it. To learn more, visit the  documentation article in C++.'
type: docs
weight: 14000
url: /cpp/aspose.words/commentrangestart/
---
## CommentRangeStart class


Denotes the start of a region of text that has a comment associated with it. To learn more, visit the [Working with Comments](https://docs.aspose.com/words/cpp/working-with-comments/) documentation article.

```cpp
class CommentRangeStart : public Aspose::Words::Node,
                          public Aspose::Words::IDisplaceableByCustomXml,
                          public Aspose::Words::INodeWithAnnotationId
```

## Methods

| Method | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor. |
| [Clone](../node/clone/)(bool) | Creates a duplicate of the node. |
| [CommentRangeStart](./commentrangestart/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, int32_t) | Initializes a new instance of this class. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Specifies custom node identifier. |
| virtual [get_Document](../node/get_document/)() const | Gets the document to which this node belongs. |
| [get_Id](./get_id/)() const | Specifies the identifier of the comment to which this region is linked. |
| virtual [get_IsComposite](../node/get_iscomposite/)() | Returns **true** if this node can contain other nodes. |
| [get_NextSibling](../node/get_nextsibling/)() | Gets the node immediately following this node. |
| [get_NodeType](./get_nodetype/)() const override | Returns [CommentRangeStart](../nodetype/). |
| [get_ParentNode](../node/get_parentnode/)() | Gets the immediate parent of this node. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Gets the node immediately preceding this node. |
| [get_Range](../node/get_range/)() | Returns a [Range](../range/) object that represents the portion of a document that is contained in this node. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Gets the first ancestor of the specified [NodeType](../nodetype/). |
| [GetAncestorOf](../node/getancestorof/)() |  |
| virtual [GetText](../node/gettext/)() | Gets the text of this node and of all its children. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gets next node according to the pre-order tree traversal algorithm. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | A utility method that converts a node type enum value into a user friendly string. |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../node/remove/)() | Removes itself from the parent. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Setter for [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_Id](./set_id/)(int32_t) | Setter for [Aspose::Words::CommentRangeStart::get_Id](./get_id/). |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exports the content of the node into a string in the specified format. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exports the content of the node into a string using the specified save options. |
| static [Type](./type/)() |  |
## Remarks


To create a comment anchored to a region of text, you need to create a [Comment](../comment/) and then create [CommentRangeStart](./) and [CommentRangeEnd](../commentrangeend/) and set their identifiers to the same [Id](../comment/get_id/) value.

[CommentRangeStart](./) is an inline-level node and can only be a child of [Paragraph](../paragraph/).

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

* Class [Node](../node/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
