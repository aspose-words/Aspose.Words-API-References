---
title: Aspose::Words::DocumentVisitor::VisitAbsolutePositionTab method
linktitle: VisitAbsolutePositionTab
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentVisitor::VisitAbsolutePositionTab method. Called when a AbsolutePositionTab node is encountered in the document in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words/documentvisitor/visitabsolutepositiontab/
---
## DocumentVisitor::VisitAbsolutePositionTab method


Called when a [AbsolutePositionTab](../../absolutepositiontab/) node is encountered in the document.

```cpp
virtual Aspose::Words::VisitorAction Aspose::Words::DocumentVisitor::VisitAbsolutePositionTab(System::SharedPtr<Aspose::Words::AbsolutePositionTab> tab)
```


| Parameter | Type | Description |
| --- | --- | --- |
| tab | System::SharedPtr\<Aspose::Words::AbsolutePositionTab\> | The object that is being visited. |

### ReturnValue

A [VisitorAction](../../visitoraction/) value that specifies how to continue the enumeration.

## Examples



Shows how to process absolute position tab characters with a document visitor. 
```cpp
void DocumentToTxt()
{
    auto doc = MakeObject<Document>(MyDir + u"Absolute position tab.docx");

    // Extract the text contents of our document by accepting this custom document visitor.
    auto myDocTextExtractor = MakeObject<ExAbsolutePositionTab::DocTextExtractor>();
    doc->get_FirstSection()->get_Body()->Accept(myDocTextExtractor);

    // The absolute position tab, which has no equivalent in string form, has been explicitly converted to a tab character.
    ASSERT_EQ(u"Before AbsolutePositionTab\tAfter AbsolutePositionTab", myDocTextExtractor->GetText());

    // An AbsolutePositionTab can accept a DocumentVisitor by itself too.
    auto absPositionTab =
        System::DynamicCast<AbsolutePositionTab>(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetChild(NodeType::SpecialChar, 0, true));

    myDocTextExtractor = MakeObject<ExAbsolutePositionTab::DocTextExtractor>();
    absPositionTab->Accept(myDocTextExtractor);

    ASSERT_EQ(u"\t", myDocTextExtractor->GetText());
}

class DocTextExtractor : public DocumentVisitor
{
public:
    DocTextExtractor()
    {
        mBuilder = MakeObject<System::Text::StringBuilder>();
    }

    VisitorAction VisitRun(SharedPtr<Run> run) override
    {
        AppendText(run->get_Text());
        return VisitorAction::Continue;
    }

    VisitorAction VisitAbsolutePositionTab(SharedPtr<AbsolutePositionTab> tab) override
    {
        mBuilder->Append(u"\t");
        return VisitorAction::Continue;
    }

    String GetText()
    {
        return mBuilder->ToString();
    }

private:
    SharedPtr<System::Text::StringBuilder> mBuilder;

    void AppendText(String text)
    {
        mBuilder->Append(text);
    }
};
```

## See Also

* Enum [VisitorAction](../../visitoraction/)
* Class [AbsolutePositionTab](../../absolutepositiontab/)
* Class [DocumentVisitor](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
