---
title: get_MathObjectType
second_title: Aspose.Words for C++ API Reference
description: Gets type MathObjectType of this Office Math object.
type: docs
weight: 66
url: /cpp/aspose.words.math/officemath/get_mathobjecttype/
---
## OfficeMath::get_MathObjectType method


Gets type [MathObjectType](./) of this Office [Math](../../) object.

```cpp
Aspose::Words::Math::MathObjectType Aspose::Words::Math::OfficeMath::get_MathObjectType() const
```


## Examples



Shows how to print the node structure of every office math node in a document. 
```cpp
void OfficeMathToText()
{
    auto doc = MakeObject<Document>(MyDir + u"DocumentVisitor-compatible features.docx");
    auto visitor = MakeObject<ExDocumentVisitor::OfficeMathStructurePrinter>();

    // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
    // and then traverses all the node's children in a depth-first manner.
    // The visitor can read and modify each visited node.
    doc->Accept(visitor);

    std::cout << visitor->GetText() << std::endl;
}

class OfficeMathStructurePrinter : public DocumentVisitor
{
public:
    OfficeMathStructurePrinter() : mVisitorIsInsideOfficeMath(false), mDocTraversalDepth(0)
    {
        mBuilder = MakeObject<System::Text::StringBuilder>();
        mVisitorIsInsideOfficeMath = false;
    }

    String GetText()
    {
        return mBuilder->ToString();
    }

    VisitorAction VisitRun(SharedPtr<Run> run) override
    {
        if (mVisitorIsInsideOfficeMath)
        {
            IndentAndAppendLine(String(u"[Run] \"") + run->GetText() + u"\"");
        }

        return VisitorAction::Continue;
    }

    VisitorAction VisitOfficeMathStart(SharedPtr<OfficeMath> officeMath) override
    {
        IndentAndAppendLine(String(u"[OfficeMath start] Math object type: ") + System::ObjectExt::ToString(officeMath->get_MathObjectType()));
        mDocTraversalDepth++;
        mVisitorIsInsideOfficeMath = true;

        return VisitorAction::Continue;
    }

    VisitorAction VisitOfficeMathEnd(SharedPtr<OfficeMath> officeMath) override
    {
        mDocTraversalDepth--;
        IndentAndAppendLine(u"[OfficeMath end]");
        mVisitorIsInsideOfficeMath = false;

        return VisitorAction::Continue;
    }

private:
    bool mVisitorIsInsideOfficeMath;
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

* Enum [MathObjectType](../../mathobjecttype/)
* Class [OfficeMath](../)
* Namespace [Aspose::Words::Math](../../)
* Library [Aspose.Words](../../../)
