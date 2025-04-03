---
title: DocumentVisitor.visitSmartTagStart method
linktitle: visitSmartTagStart method
articleTitle: visitSmartTagStart method
second_title: Aspose.Words for NodeJs
description: "DocumentVisitor.visitSmartTagStart method. Called when enumeration of a smart tag has started."
type: docs
weight: 420
url: /nodejs-net/Aspose.Words/documentvisitor/visitSmartTagStart/
---

## visitSmartTagStart(smartTag) {#smarttag}

Called when enumeration of a smart tag has started.


```js
visitSmartTagStart(smartTag: Aspose.Words.Markup.SmartTag)
```

| Parameter | Type | Description |
| --- | --- | --- |
| smartTag | [SmartTag](../../../aspose.words.markup/smarttag/) | The object that is being visited. |

### Returns

A [VisitorAction](../../visitoraction/) value that specifies how to continue the enumeration.


### Examples

Shows how to print the node structure of every smart tag in a document.

```js
test('SmartTagToText', () => {
  let doc = new aw.Document(base.myDir + "Smart tags.doc");
  let visitor = new SmartTagStructurePrinter();

  // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
  // and then traverses all the node's children in a depth-first manner.
  // The visitor can read and modify each visited node.
  doc.accept(visitor);

  console.log(visitor.getText());
});


  /// <summary>
  /// Traverses a node's non-binary tree of child nodes.
  /// Creates a map in the form of a string of all encountered SmartTag nodes and their children.
  /// </summary>
public class SmartTagStructurePrinter : DocumentVisitor
{
  public SmartTagStructurePrinter()
  {
    mBuilder = new StringBuilder();
    mVisitorIsInsideSmartTag = false;
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
    if (mVisitorIsInsideSmartTag) IndentAndAppendLine("[Run] \"" + run.getText() + "\"");

    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Called when a SmartTag node is encountered in the document.
    /// </summary>
  public override VisitorAction VisitSmartTagStart(SmartTag smartTag)
  {
    IndentAndAppendLine("[SmartTag start] Name: " + smartTag.element);
    mDocTraversalDepth++;
    mVisitorIsInsideSmartTag = true;

    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Called after all the child nodes of a SmartTag node have been visited.
    /// </summary>
  public override VisitorAction VisitSmartTagEnd(SmartTag smartTag)
  {
    mDocTraversalDepth--;
    IndentAndAppendLine("[SmartTag end]");
    mVisitorIsInsideSmartTag = false;

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

  private bool mVisitorIsInsideSmartTag;
  private int mDocTraversalDepth;
  private readonly StringBuilder mBuilder;
}
```

### See Also

* module [Aspose.Words](../../)
* class [DocumentVisitor](../)

