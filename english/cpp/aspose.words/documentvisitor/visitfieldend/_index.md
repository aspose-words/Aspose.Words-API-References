---
title: VisitFieldEnd
second_title: Aspose.Words for C++ API Reference
description: Called when a field ends in the document.
type: docs
weight: 222
url: /cpp/aspose.words/documentvisitor/visitfieldend/
---
## DocumentVisitor.VisitFieldEnd method


Called when a field ends in the document.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitFieldEnd(System::SharedPtr<Aspose::Words::Fields::FieldEnd> fieldEnd)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fieldEnd | System::SharedPtr\<Aspose::Words::Fields::FieldEnd\> | The object that is being visited. |

### ReturnValue


A [VisitorAction](../../visitoraction/) value that specifies how to continue the enumeration.

For more info see [VisitFieldStart()](../visitfieldstart/)

## Examples




Shows how to print the node structure of every field in a document. 
```cpp
void FieldToText()
{
    auto doc = MakeObject<Document>(MyDir + u"DocumentVisitor-compatible features.docx");
    auto visitor = MakeObject<ExDocumentVisitor::FieldStructurePrinter>();

    // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
    // and then traverses all the node's children in a depth-first manner.
    // The visitor can read and modify each visited node.
    doc->Accept(visitor);

    std::cout << visitor->GetText() << std::endl;
}

class FieldStructurePrinter : public DocumentVisitor
{
public:
    FieldStructurePrinter() : mVisitorIsInsideField(false), mDocTraversalDepth(0)
    {
        mBuilder = MakeObject<System::Text::StringBuilder>();
        mVisitorIsInsideField = false;
    }

    String GetText()
    {
        return mBuilder->ToString();
    }

    VisitorAction VisitRun(SharedPtr<Run> run) override
    {
        if (mVisitorIsInsideField)
        {
            IndentAndAppendLine(String(u"[Run] \"") + run->GetText() + u"\"");
        }

        return VisitorAction::Continue;
    }

    VisitorAction VisitFieldStart(SharedPtr<FieldStart> fieldStart) override
    {
        IndentAndAppendLine(String(u"[Field start] FieldType: ") + System::ObjectExt::ToString(fieldStart->get_FieldType()));
        mDocTraversalDepth++;
        mVisitorIsInsideField = true;

        return VisitorAction::Continue;
    }

    VisitorAction VisitFieldEnd(SharedPtr<FieldEnd> fieldEnd) override
    {
        mDocTraversalDepth--;
        IndentAndAppendLine(u"[Field end]");
        mVisitorIsInsideField = false;

        return VisitorAction::Continue;
    }

    VisitorAction VisitFieldSeparator(SharedPtr<FieldSeparator> fieldSeparator) override
    {
        IndentAndAppendLine(u"[FieldSeparator]");

        return VisitorAction::Continue;
    }

private:
    bool mVisitorIsInsideField;
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

