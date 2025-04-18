﻿---
title: StructuredDocumentTag.accept method
linktitle: accept method
articleTitle: accept method
second_title: Aspose.Words for Node.js
description: "StructuredDocumentTag.accept method. Accepts a visitor."
type: docs
weight: 330
url: /nodejs-net/aspose.words.markup/structureddocumenttag/accept/
---

## accept(visitor) {#documentvisitor}

Accepts a visitor.


```js
accept(visitor: Aspose.Words.DocumentVisitor)
```

| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../../aspose.words/documentvisitor/) | The visitor that will visit the nodes. |

### Remarks

Enumerates over this node and all of its children. Each node calls a corresponding method on [DocumentVisitor](../../../aspose.words/documentvisitor/).

For more info see the Visitor design pattern.




Calls [DocumentVisitor.visitStructuredDocumentTagStart()](../../../aspose.words/documentvisitor/visitStructuredDocumentTagStart/#structureddocumenttag), then calls [Node.accept()](../../../aspose.words/node/accept/#documentvisitor) for all
child nodes of the smart tag and calls [DocumentVisitor.visitStructuredDocumentTagEnd()](../../../aspose.words/documentvisitor/visitStructuredDocumentTagEnd/#structureddocumenttag) at the end.



### Returns

True if all nodes were visited; false if [DocumentVisitor](../../../aspose.words/documentvisitor/) stopped the operation before visiting all nodes.


### Examples

Shows how to print the node structure of every structured document tag in a document.

```js
test('StructuredDocumentTagToText', () => {
  let doc = new aw.Document(base.myDir + "DocumentVisitor-compatible features.docx");
  let visitor = new StructuredDocumentTagNodePrinter();

  // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
  // and then traverses all the node's children in a depth-first manner.
  // The visitor can read and modify each visited node.
  doc.accept(visitor);

  console.log(visitor.getText());
});


  /// <summary>
  /// Traverses a node's non-binary tree of child nodes.
  /// Creates a map in the form of a string of all encountered StructuredDocumentTag nodes and their children.
  /// </summary>
public class StructuredDocumentTagNodePrinter : DocumentVisitor
{
  public StructuredDocumentTagNodePrinter()
  {
    mBuilder = new StringBuilder();
    mVisitorIsInsideStructuredDocumentTag = false;
  }

    /// <summary>
    /// Gets the plain text of the document that was accumulated by the visitor.
    /// </summary>
  public string GetText()
  {
    return mBuilder.toString();
  }

    /// <summary>
    /// Called when a Run node is encountered in the document.
    /// </summary>
  public override VisitorAction VisitRun(Run run)
  {
    if (mVisitorIsInsideStructuredDocumentTag) IndentAndAppendLine("[Run] \"" + run.getText() + "\"");

    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Called when a StructuredDocumentTag node is encountered in the document.
    /// </summary>
  public override VisitorAction VisitStructuredDocumentTagStart(StructuredDocumentTag sdt)
  {
    IndentAndAppendLine("[StructuredDocumentTag start] Title: " + sdt.title);
    mDocTraversalDepth++;

    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Called after all the child nodes of a StructuredDocumentTag node have been visited.
    /// </summary>
  public override VisitorAction VisitStructuredDocumentTagEnd(StructuredDocumentTag sdt)
  {
    mDocTraversalDepth--;
    IndentAndAppendLine("[StructuredDocumentTag end]");

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

  private readonly bool mVisitorIsInsideStructuredDocumentTag;
  private int mDocTraversalDepth;
  private readonly StringBuilder mBuilder;
}
```

### See Also

* module [Aspose.Words.Markup](../../)
* class [StructuredDocumentTag](../)

