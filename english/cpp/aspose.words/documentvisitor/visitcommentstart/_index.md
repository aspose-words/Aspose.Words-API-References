---
title: VisitCommentStart
second_title: Aspose.Words for C++ API Reference
description: Called when enumeration of a comment text has started.
type: docs
weight: 196
url: /cpp/aspose.words/documentvisitor/visitcommentstart/
---
## DocumentVisitor::VisitCommentStart method


Called when enumeration of a comment text has started.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitCommentStart(System::SharedPtr<Aspose::Words::Comment> comment)
```


| Parameter | Type | Description |
| --- | --- | --- |
| comment | System::SharedPtr\<Aspose::Words::Comment\> | The object that is being visited. |

### ReturnValue

A [VisitorAction](../../visitoraction/) value that specifies how to continue the enumeration.

## Examples



Shows how to print the node structure of every comment and comment range in a document. 
```cpp
void CommentsToText()
{
    auto doc = MakeObject<Document>(MyDir + u"DocumentVisitor-compatible features.docx");
    auto visitor = MakeObject<ExDocumentVisitor::CommentStructurePrinter>();

    // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
    // and then traverses all the node's children in a depth-first manner.
    // The visitor can read and modify each visited node.
    doc->Accept(visitor);

    std::cout << visitor->GetText() << std::endl;
}

class CommentStructurePrinter : public DocumentVisitor
{
public:
    CommentStructurePrinter() : mVisitorIsInsideComment(false), mDocTraversalDepth(0)
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
            IndentAndAppendLine(String(u"[Run] \"") + run->GetText() + u"\"");
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
        IndentAndAppendLine(u"[Comment range end]");
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


Shows how to use a [DocumentVisitor](../) implementation to remove all hidden content from a document. 
```cpp
void RemoveHiddenContentFromDocument()
{
    auto doc = MakeObject<Document>(MyDir + u"Hidden content.docx");

    auto hiddenContentRemover = MakeObject<ExFont::RemoveHiddenContentVisitor>();

    // Below are three types of fields which can accept a document visitor,
    // which will allow it to visit the accepting node, and then traverse its child nodes in a depth-first manner.
    // 1 -  Paragraph node:
    auto para = System::DynamicCast<Paragraph>(doc->GetChild(NodeType::Paragraph, 4, true));
    para->Accept(hiddenContentRemover);

    // 2 -  Table node:
    SharedPtr<Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
    table->Accept(hiddenContentRemover);

    // 3 -  Document node:
    doc->Accept(hiddenContentRemover);

    doc->Save(ArtifactsDir + u"Font.RemoveHiddenContentFromDocument.docx");
}

class RemoveHiddenContentVisitor : public DocumentVisitor
{
public:
    VisitorAction VisitFieldStart(SharedPtr<FieldStart> fieldStart) override
    {
        if (fieldStart->get_Font()->get_Hidden())
        {
            fieldStart->Remove();
        }

        return VisitorAction::Continue;
    }

    VisitorAction VisitFieldEnd(SharedPtr<FieldEnd> fieldEnd) override
    {
        if (fieldEnd->get_Font()->get_Hidden())
        {
            fieldEnd->Remove();
        }

        return VisitorAction::Continue;
    }

    VisitorAction VisitFieldSeparator(SharedPtr<FieldSeparator> fieldSeparator) override
    {
        if (fieldSeparator->get_Font()->get_Hidden())
        {
            fieldSeparator->Remove();
        }

        return VisitorAction::Continue;
    }

    VisitorAction VisitRun(SharedPtr<Run> run) override
    {
        if (run->get_Font()->get_Hidden())
        {
            run->Remove();
        }

        return VisitorAction::Continue;
    }

    VisitorAction VisitParagraphStart(SharedPtr<Paragraph> paragraph) override
    {
        if (paragraph->get_ParagraphBreakFont()->get_Hidden())
        {
            paragraph->Remove();
        }

        return VisitorAction::Continue;
    }

    VisitorAction VisitFormField(SharedPtr<FormField> formField) override
    {
        if (formField->get_Font()->get_Hidden())
        {
            formField->Remove();
        }

        return VisitorAction::Continue;
    }

    VisitorAction VisitGroupShapeStart(SharedPtr<GroupShape> groupShape) override
    {
        if (groupShape->get_Font()->get_Hidden())
        {
            groupShape->Remove();
        }

        return VisitorAction::Continue;
    }

    VisitorAction VisitShapeStart(SharedPtr<Shape> shape) override
    {
        if (shape->get_Font()->get_Hidden())
        {
            shape->Remove();
        }

        return VisitorAction::Continue;
    }

    VisitorAction VisitCommentStart(SharedPtr<Comment> comment) override
    {
        if (comment->get_Font()->get_Hidden())
        {
            comment->Remove();
        }

        return VisitorAction::Continue;
    }

    VisitorAction VisitFootnoteStart(SharedPtr<Footnote> footnote) override
    {
        if (footnote->get_Font()->get_Hidden())
        {
            footnote->Remove();
        }

        return VisitorAction::Continue;
    }

    VisitorAction VisitSpecialChar(SharedPtr<SpecialChar> specialChar) override
    {
        if (specialChar->get_Font()->get_Hidden())
        {
            specialChar->Remove();
        }

        return VisitorAction::Continue;
    }

    VisitorAction VisitTableEnd(SharedPtr<Table> table) override
    {
        // The content inside table cells may have the hidden content flag, but the tables themselves cannot.
        // If this table had nothing but hidden content, this visitor would have removed all of it,
        // and there would be no child nodes left.
        // Thus, we can also treat the table itself as hidden content and remove it.
        // Tables which are empty but do not have hidden content will have cells with empty paragraphs inside,
        // which this visitor will not remove.
        if (!table->get_HasChildNodes())
        {
            table->Remove();
        }

        return VisitorAction::Continue;
    }

    VisitorAction VisitCellEnd(SharedPtr<Cell> cell) override
    {
        if (!cell->get_HasChildNodes() && cell->get_ParentNode() != nullptr)
        {
            cell->Remove();
        }

        return VisitorAction::Continue;
    }

    VisitorAction VisitRowEnd(SharedPtr<Row> row) override
    {
        if (!row->get_HasChildNodes() && row->get_ParentNode() != nullptr)
        {
            row->Remove();
        }

        return VisitorAction::Continue;
    }
};
```

## See Also

* Enum [VisitorAction](../../visitoraction/)
* Class [Comment](../../comment/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
