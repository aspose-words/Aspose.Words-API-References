---
title: OfficeMath.accept method
linktitle: accept method
articleTitle: accept method
second_title: Aspose.Words for NodeJs
description: "OfficeMath.accept method. Accepts a visitor."
type: docs
weight: 60
url: /nodejs-net/Aspose.Words.Math/officemath/accept/
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




Calls [DocumentVisitor.visitOfficeMathStart()](../../../aspose.words/documentvisitor/visitOfficeMathStart/#officemath), then calls [Node.accept()](../../../aspose.words/node/accept/#documentvisitor) for all
child nodes of the Office Math and calls [DocumentVisitor.visitOfficeMathEnd()](../../../aspose.words/documentvisitor/visitOfficeMathEnd/#officemath) at the end.



### Returns

True if all nodes were visited; false if [DocumentVisitor](../../../aspose.words/documentvisitor/) stopped the operation before visiting all nodes.


### Examples

Shows how to print the node structure of every office math node in a document.

```js
test('OfficeMathToText', () => {
  let doc = new aw.Document(base.myDir + "DocumentVisitor-compatible features.docx");
  let visitor = new OfficeMathStructurePrinter();

  // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
  // and then traverses all the node's children in a depth-first manner.
  // The visitor can read and modify each visited node.
  doc.accept(visitor);

  console.log(visitor.getText());
});


  /// <summary>
  /// Traverses a node's non-binary tree of child nodes.
  /// Creates a map in the form of a string of all encountered OfficeMath nodes and their children.
  /// </summary>
public class OfficeMathStructurePrinter : DocumentVisitor
{
  public OfficeMathStructurePrinter()
  {
    mBuilder = new StringBuilder();
    mVisitorIsInsideOfficeMath = false;
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
    if (mVisitorIsInsideOfficeMath) IndentAndAppendLine("[Run] \"" + run.getText() + "\"");

    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Called when an OfficeMath node is encountered in the document.
    /// </summary>
  public override VisitorAction VisitOfficeMathStart(OfficeMath officeMath)
  {
    IndentAndAppendLine("[OfficeMath start] Math object type: " + officeMath.mathObjectType);
    mDocTraversalDepth++;
    mVisitorIsInsideOfficeMath = true;

    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Called after all the child nodes of an OfficeMath node have been visited.
    /// </summary>
  public override VisitorAction VisitOfficeMathEnd(OfficeMath officeMath)
  {
    mDocTraversalDepth--;
    IndentAndAppendLine("[OfficeMath end]");
    mVisitorIsInsideOfficeMath = false;

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

  private bool mVisitorIsInsideOfficeMath;
  private int mDocTraversalDepth;
  private readonly StringBuilder mBuilder;
}
```

### See Also

* module [Aspose.Words.Math](../../)
* class [OfficeMath](../)

