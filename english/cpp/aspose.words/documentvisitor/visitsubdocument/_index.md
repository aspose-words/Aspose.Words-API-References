---
title: Aspose::Words::DocumentVisitor::VisitSubDocument method
linktitle: VisitSubDocument
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentVisitor::VisitSubDocument method. Called when a sub-document is encountered in C++.'
type: docs
weight: 51000
url: /cpp/aspose.words/documentvisitor/visitsubdocument/
---
## DocumentVisitor::VisitSubDocument method


Called when a sub-document is encountered.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitSubDocument(System::SharedPtr<Aspose::Words::SubDocument> subDocument)
```


| Parameter | Type | Description |
| --- | --- | --- |
| subDocument | System::SharedPtr\<Aspose::Words::SubDocument\> | The object that is being visited. |

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

## See Also

* Enum [VisitorAction](../../visitoraction/)
* Class [SubDocument](../../subdocument/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
