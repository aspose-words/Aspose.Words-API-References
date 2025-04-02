---
title: Footnote.accept method
linktitle: accept method
articleTitle: accept method
second_title: Aspose.Words for NodeJs
description: "Footnote.accept method. Accepts a visitor."
type: docs
weight: 80
url: /nodejs-net/Aspose.Words.Notes/footnote/accept/
---

## accept(visitor) {#documentvisitor}

Accepts a visitor.


```js
accept(visitor: Aspose.Words.DocumentVisitor)
```

| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../../Aspose.Words/documentvisitor/) | The visitor that will visit the nodes. |

### Remarks

Enumerates over this node and all of its children. Each node calls a corresponding method on [DocumentVisitor](../../../Aspose.Words/documentvisitor/).

For more info see the Visitor design pattern.




Calls DocumentVisitor.VisitFootnoteStart, then calls Accept for all child nodes of the footnote
and calls DocumentVisitor.VisitFootnoteEnd at the end.


### Returns

True if all nodes were visited; false if [DocumentVisitor](../../../Aspose.Words/documentvisitor/) stopped the operation before visiting all nodes.


### Examples

Shows how to print the node structure of every footnote in a document.

```js
test('FootnoteToText', () => {
  let doc = new aw.Document(base.myDir + "DocumentVisitor-compatible features.docx");
  let visitor = new FootnoteStructurePrinter();

  // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
  // and then traverses all the node's children in a depth-first manner.
  // The visitor can read and modify each visited node.
  doc.accept(visitor);

  console.log(visitor.getText());
});


  /// <summary>
  /// Traverses a node's non-binary tree of child nodes.
  /// Creates a map in the form of a string of all encountered Footnote nodes and their children.
  /// </summary>
public class FootnoteStructurePrinter : DocumentVisitor
{
  public FootnoteStructurePrinter()
  {
    mBuilder = new StringBuilder();
    mVisitorIsInsideFootnote = false;
  }

    /// <summary>
    /// Gets the plain text of the document that was accumulated by the visitor.
    /// </summary>
  public string GetText()
  {
    return mBuilder.toString();
  }

    /// <summary>
    /// Called when a Footnote node is encountered in the document.
    /// </summary>
  public override VisitorAction VisitFootnoteStart(Footnote footnote)
  {
    IndentAndAppendLine("[Footnote start] Type: " + footnote.footnoteType);
    mDocTraversalDepth++;
    mVisitorIsInsideFootnote = true;

    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Called after all the child nodes of a Footnote node have been visited.
    /// </summary>
  public override VisitorAction VisitFootnoteEnd(Footnote footnote)
  {
    mDocTraversalDepth--;
    IndentAndAppendLine("[Footnote end]");
    mVisitorIsInsideFootnote = false;

    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Called when a Run node is encountered in the document.
    /// </summary>
  public override VisitorAction VisitRun(Run run)
  {
    if (mVisitorIsInsideFootnote) IndentAndAppendLine("[Run] \"" + run.getText() + "\"");

    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
    /// </summary>
    /// <param name="text"></param>
  private void IndentAndAppendLine(string text)
  {
    for (let i = 0; i < mDocTraversalDepth; i++) mBuilder.append("|  ");

    mBuilder.AppendLine(text);
  }

  private bool mVisitorIsInsideFootnote;
  private int mDocTraversalDepth;
  private readonly StringBuilder mBuilder;
}
```

### See Also

* module [Aspose.Words.Notes](../../)
* class [Footnote](../)

