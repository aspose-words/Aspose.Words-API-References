---
title: Aspose::Words::DocumentVisitor::VisitStructuredDocumentTagEnd method
linktitle: VisitStructuredDocumentTagEnd
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentVisitor::VisitStructuredDocumentTagEnd method. Called when enumeration of a structured document tag has ended in C++.'
type: docs
weight: 47000
url: /cpp/aspose.words/documentvisitor/visitstructureddocumenttagend/
---
## DocumentVisitor::VisitStructuredDocumentTagEnd method


Called when enumeration of a structured document tag has ended.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitStructuredDocumentTagEnd(System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> sdt)
```


| Parameter | Type | Description |
| --- | --- | --- |
| sdt | System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\> | The object that is being visited. |

### ReturnValue

A [VisitorAction](../../visitoraction/) value that specifies how to continue the enumeration.

## Examples



Shows how to print the node structure of every structured document tag in a document. 
```cpp
void StructuredDocumentTagToText()
{
    auto doc = MakeObject<Document>(MyDir + u"DocumentVisitor-compatible features.docx");
    auto visitor = MakeObject<ExDocumentVisitor::StructuredDocumentTagNodePrinter>();

    // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
    // and then traverses all the node's children in a depth-first manner.
    // The visitor can read and modify each visited node.
    doc->Accept(visitor);

    std::cout << visitor->GetText() << std::endl;
}

class StructuredDocumentTagNodePrinter : public DocumentVisitor
{
public:
    StructuredDocumentTagNodePrinter() : mVisitorIsInsideStructuredDocumentTag(false), mDocTraversalDepth(0)
    {
        mBuilder = MakeObject<System::Text::StringBuilder>();
        mVisitorIsInsideStructuredDocumentTag = false;
    }

    String GetText()
    {
        return mBuilder->ToString();
    }

    VisitorAction VisitRun(SharedPtr<Run> run) override
    {
        if (mVisitorIsInsideStructuredDocumentTag)
        {
            IndentAndAppendLine(String(u"[Run] \"") + run->GetText() + u"\"");
        }

        return VisitorAction::Continue;
    }

    VisitorAction VisitStructuredDocumentTagStart(SharedPtr<StructuredDocumentTag> sdt) override
    {
        IndentAndAppendLine(String(u"[StructuredDocumentTag start] Title: ") + sdt->get_Title());
        mDocTraversalDepth++;

        return VisitorAction::Continue;
    }

    VisitorAction VisitStructuredDocumentTagEnd(SharedPtr<StructuredDocumentTag> sdt) override
    {
        mDocTraversalDepth--;
        IndentAndAppendLine(u"[StructuredDocumentTag end]");

        return VisitorAction::Continue;
    }

private:
    bool mVisitorIsInsideStructuredDocumentTag;
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

* Enum [VisitorAction](../../visitoraction/)
* Class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
