---
title: DocumentVisitor.visitStructuredDocumentTagStart method
linktitle: visitStructuredDocumentTagStart method
articleTitle: visitStructuredDocumentTagStart method
second_title: Aspose.Words for NodeJs
description: "DocumentVisitor.visitStructuredDocumentTagStart method. Called when enumeration of a structured document tag has started."
type: docs
weight: 470
url: /nodejs-net/Aspose.Words/documentvisitor/visitStructuredDocumentTagStart/
---

## visitStructuredDocumentTagStart(sdt) {#structureddocumenttag}

Called when enumeration of a structured document tag has started.


```js
visitStructuredDocumentTagStart(sdt: Aspose.Words.Markup.StructuredDocumentTag)
```

| Parameter | Type | Description |
| --- | --- | --- |
| sdt | [StructuredDocumentTag](../../../Aspose.Words.Markup/structureddocumenttag/) | The object that is being visited. |

### Returns

A [VisitorAction](../../visitoraction/) value that specifies how to continue the enumeration.


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

* module [Aspose.Words](../../)
* class [DocumentVisitor](../)

