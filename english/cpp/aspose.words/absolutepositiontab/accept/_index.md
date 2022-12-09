---
title: Accept
second_title: Aspose.Words for C++ API Reference
description: Accepts a visitor.
type: docs
weight: 14
url: /cpp/aspose.words/absolutepositiontab/accept/
---
## AbsolutePositionTab::Accept method


Accepts a visitor.

```cpp
bool Aspose::Words::AbsolutePositionTab::Accept(System::SharedPtr<Aspose::Words::DocumentVisitor> visitor) override
```


| Parameter | Type | Description |
| --- | --- | --- |
| visitor | System::SharedPtr\<Aspose::Words::DocumentVisitor\> | The visitor that will visit the node. |

### ReturnValue

**false** if the visitor requested the enumeration to stop.
## Remarks


Calls [VisitAbsolutePositionTab()](../../documentvisitor/visitabsolutepositiontab/).

For more info see the Visitor design pattern.

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

* Class [DocumentVisitor](../../documentvisitor/)
* Class [AbsolutePositionTab](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
