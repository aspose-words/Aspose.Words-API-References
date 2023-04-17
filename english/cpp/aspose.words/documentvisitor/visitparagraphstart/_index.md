---
title: Aspose::Words::DocumentVisitor::VisitParagraphStart method
linktitle: VisitParagraphStart
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentVisitor::VisitParagraphStart method. Called when enumeration of a paragraph has started in C++.'
type: docs
weight: 36000
url: /cpp/aspose.words/documentvisitor/visitparagraphstart/
---
## DocumentVisitor::VisitParagraphStart method


Called when enumeration of a paragraph has started.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitParagraphStart(System::SharedPtr<Aspose::Words::Paragraph> paragraph)
```


| Parameter | Type | Description |
| --- | --- | --- |
| paragraph | System::SharedPtr\<Aspose::Words::Paragraph\> | The object that is being visited. |

### ReturnValue

A [VisitorAction](../../visitoraction/) value that specifies how to continue the enumeration.

## Examples



Shows how to use a document visitor to print a document's node structure. 
```cpp
void DocStructureToText()
{
    auto doc = MakeObject<Document>(MyDir + u"DocumentVisitor-compatible features.docx");
    auto visitor = MakeObject<ExDocumentVisitor::DocStructurePrinter>();

    // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
    // and then traverses all the node's children in a depth-first manner.
    // The visitor can read and modify each visited node.
    doc->Accept(visitor);

    std::cout << visitor->GetText() << std::endl;
}

class DocStructurePrinter : public DocumentVisitor
{
public:
    DocStructurePrinter() : mDocTraversalDepth(0)
    {
        mAcceptingNodeChildTree = MakeObject<System::Text::StringBuilder>();
    }

    String GetText()
    {
        return mAcceptingNodeChildTree->ToString();
    }

    VisitorAction VisitDocumentStart(SharedPtr<Document> doc) override
    {
        int childNodeCount = doc->GetChildNodes(NodeType::Any, true)->get_Count();

        IndentAndAppendLine(String(u"[Document start] Child nodes: ") + childNodeCount);
        mDocTraversalDepth++;

        // Allow the visitor to continue visiting other nodes.
        return VisitorAction::Continue;
    }

    VisitorAction VisitDocumentEnd(SharedPtr<Document> doc) override
    {
        mDocTraversalDepth--;
        IndentAndAppendLine(u"[Document end]");

        return VisitorAction::Continue;
    }

    VisitorAction VisitSectionStart(SharedPtr<Section> section) override
    {
        // Get the index of our section within the document.
        SharedPtr<NodeCollection> docSections = section->get_Document()->GetChildNodes(NodeType::Section, false);
        int sectionIndex = docSections->IndexOf(section);

        IndentAndAppendLine(String(u"[Section start] Section index: ") + sectionIndex);
        mDocTraversalDepth++;

        return VisitorAction::Continue;
    }

    VisitorAction VisitSectionEnd(SharedPtr<Section> section) override
    {
        mDocTraversalDepth--;
        IndentAndAppendLine(u"[Section end]");

        return VisitorAction::Continue;
    }

    VisitorAction VisitBodyStart(SharedPtr<Body> body) override
    {
        int paragraphCount = body->get_Paragraphs()->get_Count();
        IndentAndAppendLine(String(u"[Body start] Paragraphs: ") + paragraphCount);
        mDocTraversalDepth++;

        return VisitorAction::Continue;
    }

    VisitorAction VisitBodyEnd(SharedPtr<Body> body) override
    {
        mDocTraversalDepth--;
        IndentAndAppendLine(u"[Body end]");

        return VisitorAction::Continue;
    }

    VisitorAction VisitParagraphStart(SharedPtr<Paragraph> paragraph) override
    {
        IndentAndAppendLine(u"[Paragraph start]");
        mDocTraversalDepth++;

        return VisitorAction::Continue;
    }

    VisitorAction VisitParagraphEnd(SharedPtr<Paragraph> paragraph) override
    {
        mDocTraversalDepth--;
        IndentAndAppendLine(u"[Paragraph end]");

        return VisitorAction::Continue;
    }

    VisitorAction VisitRun(SharedPtr<Run> run) override
    {
        IndentAndAppendLine(String(u"[Run] \"") + run->GetText() + u"\"");

        return VisitorAction::Continue;
    }

    VisitorAction VisitSubDocument(SharedPtr<SubDocument> subDocument) override
    {
        IndentAndAppendLine(u"[SubDocument]");

        return VisitorAction::Continue;
    }

private:
    int mDocTraversalDepth;
    SharedPtr<System::Text::StringBuilder> mAcceptingNodeChildTree;

    void IndentAndAppendLine(String text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++)
        {
            mAcceptingNodeChildTree->Append(u"|  ");
        }

        mAcceptingNodeChildTree->AppendLine(text);
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
* Class [Paragraph](../../paragraph/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
