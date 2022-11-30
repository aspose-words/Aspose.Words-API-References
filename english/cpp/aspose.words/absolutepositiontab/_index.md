---
title: AbsolutePositionTab
second_title: Aspose.Words for C++ API Reference
description: An absolute position tab is a character which is used to advance the position on the current line of text when displaying this WordprocessingML content.
type: docs
weight: 1
url: /cpp/aspose.words/absolutepositiontab/
---
## AbsolutePositionTab class


An absolute position tab is a character which is used to advance the position on the current line of text when displaying this WordprocessingML content.

```cpp
class AbsolutePositionTab : public Aspose::Words::SpecialChar
```

## Methods

| Method | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor. |
| [Clone](../node/clone/)(bool) | Creates a duplicate of the node. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Specifies custom node identifier. |
| virtual [get_Document](../node/get_document/)() const | Gets the document to which this node belongs. |
| [get_Font](../inline/get_font/)() | Provides access to the font formatting of this object. |
| virtual [get_IsComposite](../node/get_iscomposite/)() | Returns true if this node can contain other nodes. |
| [get_IsDeleteRevision](../inline/get_isdeleterevision/)() | Returns true if this object was deleted in Microsoft Word while change tracking was enabled. |
| [get_IsFormatRevision](../inline/get_isformatrevision/)() | Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled. |
| [get_IsInsertRevision](../inline/get_isinsertrevision/)() | Returns true if this object was inserted in Microsoft Word while change tracking was enabled. |
| [get_IsMoveFromRevision](../inline/get_ismovefromrevision/)() | Returns **true** if this object was moved (deleted) in Microsoft Word while change tracking was enabled. |
| [get_IsMoveToRevision](../inline/get_ismovetorevision/)() | Returns **true** if this object was moved (inserted) in Microsoft Word while change tracking was enabled. |
| [get_NextSibling](../node/get_nextsibling/)() | Gets the node immediately following this node. |
| [get_NodeType](../specialchar/get_nodetype/)() const override | Returns **NodeType.SpecialChar**. |
| [get_ParentNode](../node/get_parentnode/)() | Gets the immediate parent of this node. |
| [get_ParentParagraph](../inline/get_parentparagraph/)() | Retrieves the parent [Paragraph](../paragraph/) of this node. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Gets the node immediately preceding this node. |
| [get_Range](../node/get_range/)() | Returns a **Range** object that represents the portion of a document that is contained in this node. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Gets the first ancestor of the specified [NodeType](../nodetype/). |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetText](../specialchar/gettext/)() override | Gets the special character that this node represents. |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gets next node according to the pre-order tree traversal algorithm. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | A utility method that converts a node type enum value into a user friendly string. |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../node/remove/)() | Removes itself from the parent. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Setter for [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exports the content of the node into a string in the specified format. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exports the content of the node into a string using the specified save options. |

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

* Class [SpecialChar](../specialchar/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words](../../)
