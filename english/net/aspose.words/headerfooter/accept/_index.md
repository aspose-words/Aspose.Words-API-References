---
title: HeaderFooter.Accept
linktitle: Accept
second_title: Aspose.Words for .NET API Reference
description: HeaderFooter Accept method. Accepts a visitor in C#.
type: docs
weight: 70
url: /net/aspose.words/headerfooter/accept/
---
## HeaderFooter.Accept method

Accepts a visitor.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Parameter | Type | Description |
| --- | --- | --- |
| visitor | DocumentVisitor | The visitor that will visit the nodes. |

### Return Value

True if all nodes were visited; false if [`DocumentVisitor`](../../documentvisitor/) stopped the operation before visiting all nodes.

## Remarks

Enumerates over this node and all of its children. Each node calls a corresponding method on [`DocumentVisitor`](../../documentvisitor/).

For more info see the Visitor design pattern.

Calls [`VisitHeaderFooterStart`](../../documentvisitor/visitheaderfooterstart/), then calls [`Accept`](../../node/accept/) for all child nodes of the section and calls [`VisitHeaderFooterEnd`](../../documentvisitor/visitheaderfooterend/) at the end.

## Examples

Shows how to print the node structure of every header and footer in a document.

```csharp
public void HeaderFooterToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    HeaderFooterStructurePrinter visitor = new HeaderFooterStructurePrinter();

    // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
    // and then traverses all the node's children in a depth-first manner.
    // The visitor can read and modify each visited node.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());

    // An alternative way of accessing a document's header/footers section-by-section is by accessing the collection.
    HeaderFooter[] headerFooters = doc.FirstSection.HeadersFooters.ToArray();
    Assert.AreEqual(3, headerFooters.Length);
}

/// <summary>
/// Traverses a node's non-binary tree of child nodes.
/// Creates a map in the form of a string of all encountered HeaderFooter nodes and their children.
/// </summary>
public class HeaderFooterStructurePrinter : DocumentVisitor
{
    public HeaderFooterStructurePrinter()
    {
        mBuilder = new StringBuilder();
        mVisitorIsInsideHeaderFooter = false;
    }

    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Called when a Run node is encountered in the document.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideHeaderFooter) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Called when a HeaderFooter node is encountered in the document.
    /// </summary>
    public override VisitorAction VisitHeaderFooterStart(HeaderFooter headerFooter)
    {
        IndentAndAppendLine("[HeaderFooter start] HeaderFooterType: " + headerFooter.HeaderFooterType);
        mDocTraversalDepth++;
        mVisitorIsInsideHeaderFooter = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Called after all the child nodes of a HeaderFooter node have been visited.
    /// </summary>
    public override VisitorAction VisitHeaderFooterEnd(HeaderFooter headerFooter)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[HeaderFooter end]");
        mVisitorIsInsideHeaderFooter = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Append a line to the StringBuilder, and indent it depending on how deep the visitor is into the document tree.
    /// </summary>
    /// <param name="text"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++) mBuilder.Append("|  ");

        mBuilder.AppendLine(text);
    }

    private bool mVisitorIsInsideHeaderFooter;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### See Also

* class [DocumentVisitor](../../documentvisitor/)
* class [HeaderFooter](../)
* namespace [Aspose.Words](../../headerfooter/)
* assembly [Aspose.Words](../../../)
