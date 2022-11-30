---
title: VisitSmartTagEnd
second_title: Aspose.Words for C++ API Reference
description: Called when enumeration of a smart tag has ended.
type: docs
weight: 521
url: /cpp/aspose.words/documentvisitor/visitsmarttagend/
---
## DocumentVisitor::VisitSmartTagEnd method


Called when enumeration of a smart tag has ended.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitSmartTagEnd(System::SharedPtr<Aspose::Words::Markup::SmartTag> smartTag)
```


| Parameter | Type | Description |
| --- | --- | --- |
| smartTag | System::SharedPtr\<Aspose::Words::Markup::SmartTag\> | The object that is being visited. |

### ReturnValue

A [VisitorAction](../../visitoraction/) value that specifies how to continue the enumeration.

## Examples



Shows how to print the node structure of every smart tag in a document. 
```cpp
void SmartTagToText()
{
    auto doc = MakeObject<Document>(MyDir + u"Smart tags.doc");
    auto visitor = MakeObject<ExDocumentVisitor::SmartTagStructurePrinter>();

    // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
    // and then traverses all the node's children in a depth-first manner.
    // The visitor can read and modify each visited node.
    doc->Accept(visitor);

    std::cout << visitor->GetText() << std::endl;
}

class SmartTagStructurePrinter : public DocumentVisitor
{
public:
    SmartTagStructurePrinter() : mVisitorIsInsideSmartTag(false), mDocTraversalDepth(0)
    {
        mBuilder = MakeObject<System::Text::StringBuilder>();
        mVisitorIsInsideSmartTag = false;
    }

    String GetText()
    {
        return mBuilder->ToString();
    }

    VisitorAction VisitRun(SharedPtr<Run> run) override
    {
        if (mVisitorIsInsideSmartTag)
        {
            IndentAndAppendLine(String(u"[Run] \"") + run->GetText() + u"\"");
        }

        return VisitorAction::Continue;
    }

    VisitorAction VisitSmartTagStart(SharedPtr<SmartTag> smartTag) override
    {
        IndentAndAppendLine(String(u"[SmartTag start] Name: ") + smartTag->get_Element());
        mDocTraversalDepth++;
        mVisitorIsInsideSmartTag = true;

        return VisitorAction::Continue;
    }

    VisitorAction VisitSmartTagEnd(SharedPtr<SmartTag> smartTag) override
    {
        mDocTraversalDepth--;
        IndentAndAppendLine(u"[SmartTag end]");
        mVisitorIsInsideSmartTag = false;

        return VisitorAction::Continue;
    }

private:
    bool mVisitorIsInsideSmartTag;
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
* Class [SmartTag](../../../aspose.words.markup/smarttag/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
