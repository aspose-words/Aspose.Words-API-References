---
title: Accept
second_title: Aspose.Words for C++ API Reference
description: Accepts a visitor.
type: docs
weight: 14
url: /cpp/aspose.words.notes/footnote/accept/
---
## Footnote::Accept method


Accepts a visitor.

```cpp
bool Aspose::Words::Notes::Footnote::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parameter | Type | Description |
| --- | --- | --- |
| visitor | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | The visitor that will visit the nodes. |

### ReturnValue

True if all nodes were visited; false if [DocumentVisitor](../../../aspose.words/documentvisitor/) stopped the operation before visiting all nodes.
## Remarks


Enumerates over this node and all of its children. Each node calls a corresponding method on [DocumentVisitor](../../../aspose.words/documentvisitor/).

For more info see the Visitor design pattern.

## Examples



Shows how to print the node structure of every footnote in a document. 
```cpp
void FootnoteToText()
{
    auto doc = MakeObject<Document>(MyDir + u"DocumentVisitor-compatible features.docx");
    auto visitor = MakeObject<ExDocumentVisitor::FootnoteStructurePrinter>();

    // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
    // and then traverses all the node's children in a depth-first manner.
    // The visitor can read and modify each visited node.
    doc->Accept(visitor);

    std::cout << visitor->GetText() << std::endl;
}

class FootnoteStructurePrinter : public DocumentVisitor
{
public:
    FootnoteStructurePrinter() : mVisitorIsInsideFootnote(false), mDocTraversalDepth(0)
    {
        mBuilder = MakeObject<System::Text::StringBuilder>();
        mVisitorIsInsideFootnote = false;
    }

    String GetText()
    {
        return mBuilder->ToString();
    }

    VisitorAction VisitFootnoteStart(SharedPtr<Footnote> footnote) override
    {
        IndentAndAppendLine(String(u"[Footnote start] Type: ") + System::ObjectExt::ToString(footnote->get_FootnoteType()));
        mDocTraversalDepth++;
        mVisitorIsInsideFootnote = true;

        return VisitorAction::Continue;
    }

    VisitorAction VisitFootnoteEnd(SharedPtr<Footnote> footnote) override
    {
        mDocTraversalDepth--;
        IndentAndAppendLine(u"[Footnote end]");
        mVisitorIsInsideFootnote = false;

        return VisitorAction::Continue;
    }

    VisitorAction VisitRun(SharedPtr<Run> run) override
    {
        if (mVisitorIsInsideFootnote)
        {
            IndentAndAppendLine(String(u"[Run] \"") + run->GetText() + u"\"");
        }

        return VisitorAction::Continue;
    }

private:
    bool mVisitorIsInsideFootnote;
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

* Class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* Class [Footnote](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words](../../../)
