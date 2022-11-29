---
title: VisitFootnoteEnd
second_title: Aspose.Words for C++ API Reference
description: Called when enumeration of a footnote or endnote text has ended.
type: docs
weight: 261
url: /cpp/aspose.words/documentvisitor/visitfootnoteend/
---
## DocumentVisitor::VisitFootnoteEnd method


Called when enumeration of a footnote or endnote text has ended.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitFootnoteEnd(System::SharedPtr<Aspose::Words::Notes::Footnote> footnote)
```


| Parameter | Type | Description |
| --- | --- | --- |
| footnote | System::SharedPtr\<Aspose::Words::Notes::Footnote\> | The object that is being visited. |

### ReturnValue

A [VisitorAction](../../visitoraction/) value that specifies how to continue the enumeration.

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

* Enum [VisitorAction](../../visitoraction/)
* Class [Footnote](../../../aspose.words.notes/footnote/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
