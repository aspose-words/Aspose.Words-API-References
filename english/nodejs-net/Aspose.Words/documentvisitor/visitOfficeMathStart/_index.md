---
title: DocumentVisitor.visitOfficeMathStart method
linktitle: visitOfficeMathStart method
articleTitle: visitOfficeMathStart method
second_title: Aspose.Words for NodeJs
description: "DocumentVisitor.visitOfficeMathStart method. Called when enumeration of a Office Math object has started."
type: docs
weight: 310
url: /nodejs-net/Aspose.Words/documentvisitor/visitOfficeMathStart/
---

## visitOfficeMathStart(officeMath) {#officemath}

Called when enumeration of a Office Math object has started.


```js
visitOfficeMathStart(officeMath: Aspose.Words.Math.OfficeMath)
```

| Parameter | Type | Description |
| --- | --- | --- |
| officeMath | [OfficeMath](../../../Aspose.Words.Math/officemath/) | The object that is being visited. |

### Returns

A [VisitorAction](../../visitoraction/) value that specifies how to continue the enumeration.


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

* module [Aspose.Words](../../)
* class [DocumentVisitor](../)

