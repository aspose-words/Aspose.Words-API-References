---
title: AbsolutePositionTab.Accept
linktitle: Accept
second_title: Aspose.Words for .NET API Reference
description: AbsolutePositionTab Accept method. Accepts a visitor in C#.
type: docs
weight: 10
url: /net/aspose.words/absolutepositiontab/accept/
---
## Accept method

Accepts a visitor.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Parameter | Type | Description |
| --- | --- | --- |
| visitor | DocumentVisitor | The visitor that will visit the node. |

### Return Value

`false` if the visitor requested the enumeration to stop.

## Remarks

Calls [`VisitAbsolutePositionTab`](../../documentvisitor/visitabsolutepositiontab/).

For more info see the Visitor design pattern.

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

* class [DocumentVisitor](../../documentvisitor/)
* class [AbsolutePositionTab](../)
* namespace [Aspose.Words](../../absolutepositiontab/)
* assembly [Aspose.Words](../../../)
