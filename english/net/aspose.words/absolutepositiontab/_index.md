---
title: AbsolutePositionTab
second_title: Aspose.Words for .NET API Reference
description: An absolute position tab is a character which is used to advance the position on the current line of text when displaying this WordprocessingML content.
type: docs
weight: 10
url: /net/aspose.words/absolutepositiontab/
---
## AbsolutePositionTab class

An absolute position tab is a character which is used to advance the position on the current line of text when displaying this WordprocessingML content.

```csharp
public class AbsolutePositionTab : SpecialChar
```

## Properties

| Name | Description |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Specifies custom node identifier. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Gets the document to which this node belongs. |
| [Font](../../aspose.words/inline/font/) { get; } | Provides access to the font formatting of this object. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Returns true if this node can contain other nodes. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Returns true if this object was deleted in Microsoft Word while change tracking was enabled. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Returns true if this object was inserted in Microsoft Word while change tracking was enabled. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | Returns **true** if this object was moved (deleted) in Microsoft Word while change tracking was enabled. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | Returns **true** if this object was moved (inserted) in Microsoft Word while change tracking was enabled. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Gets the node immediately following this node. |
| override [NodeType](../../aspose.words/specialchar/nodetype/) { get; } | Returns **NodeType.SpecialChar**. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Gets the immediate parent of this node. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Retrieves the parent [`Paragraph`](../paragraph/) of this node. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Gets the node immediately preceding this node. |
| [Range](../../aspose.words/node/range/) { get; } | Returns a **Range** object that represents the portion of a document that is contained in this node. |

## Methods

| Name | Description |
| --- | --- |
| override [Accept](../../aspose.words/absolutepositiontab/accept/)(DocumentVisitor) | Accepts a visitor. |
| [Clone](../../aspose.words/node/clone/)(bool) | Creates a duplicate of the node. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Gets the first ancestor of the specified [`NodeType`](../nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Gets the first ancestor of the specified object type. |
| override [GetText](../../aspose.words/specialchar/gettext/)() | Gets the special character that this node represents. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Gets next node according to the pre-order tree traversal algorithm. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../../aspose.words/node/remove/)() | Removes itself from the parent. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exports the content of the node into a string in the specified format. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exports the content of the node into a string using the specified save options. |

## Examples

Shows how to process absolute position tab characters with a document visitor.

```csharp
public void DocumentToTxt()
{
    Document doc = new Document(MyDir + "Absolute position tab.docx");

    // Extract the text contents of our document by accepting this custom document visitor.
    DocTextExtractor myDocTextExtractor = new DocTextExtractor();
    doc.FirstSection.Body.Accept(myDocTextExtractor);

    // The absolute position tab, which has no equivalent in string form, has been explicitly converted to a tab character.
    Assert.AreEqual("Before AbsolutePositionTab\tAfter AbsolutePositionTab", myDocTextExtractor.GetText());

    // An AbsolutePositionTab can accept a DocumentVisitor by itself too.
    AbsolutePositionTab absPositionTab = (AbsolutePositionTab)doc.FirstSection.Body.FirstParagraph.GetChild(NodeType.SpecialChar, 0, true);

    myDocTextExtractor = new DocTextExtractor();
    absPositionTab.Accept(myDocTextExtractor);

    Assert.AreEqual("\t", myDocTextExtractor.GetText());
}

/// <summary>
/// Collects the text contents of all runs in the visited document. Replaces all absolute tab characters with ordinary tabs.
/// </summary>
public class DocTextExtractor : DocumentVisitor
{
    public DocTextExtractor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// Called when a Run node is encountered in the document.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        AppendText(run.Text);
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Called when an AbsolutePositionTab node is encountered in the document.
    /// </summary>
    public override VisitorAction VisitAbsolutePositionTab(AbsolutePositionTab tab)
    {
        mBuilder.Append("\t");
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Adds text to the current output. Honors the enabled/disabled output flag.
    /// </summary>
    private void AppendText(string text)
    {
        mBuilder.Append(text);
    }

    /// <summary>
    /// Plain text of the document that was accumulated by the visitor.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    private readonly StringBuilder mBuilder;
}
```

### See Also

* class [SpecialChar](../specialchar/)
* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
