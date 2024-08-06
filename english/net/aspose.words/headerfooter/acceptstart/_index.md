---
title: HeaderFooter.AcceptStart
linktitle: AcceptStart
articleTitle: AcceptStart
second_title: Aspose.Words for .NET
description: HeaderFooter AcceptStart method. Accepts a visitor for visiting the start of the header in C#.
type: docs
weight: 90
url: /net/aspose.words/headerfooter/acceptstart/
---
## HeaderFooter.AcceptStart method

Accepts a visitor for visiting the start of the header.

```csharp
public override VisitorAction AcceptStart(DocumentVisitor visitor)
```

| Parameter | Type | Description |
| --- | --- | --- |
| visitor | DocumentVisitor | The document visitor. |

### Return Value

The action to be taken by the visitor.

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

* enum [VisitorAction](../../visitoraction/)
* class [DocumentVisitor](../../documentvisitor/)
* class [HeaderFooter](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
