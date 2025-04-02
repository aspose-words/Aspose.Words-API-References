---
title: DocumentVisitor.visitEditableRangeEnd method
linktitle: visitEditableRangeEnd method
articleTitle: visitEditableRangeEnd method
second_title: Aspose.Words for NodeJs
description: "DocumentVisitor.visitEditableRangeEnd method. Called when an end of an editable range is encountered in the document."
type: docs
weight: 160
url: /nodejs-net/Aspose.Words/documentvisitor/visitEditableRangeEnd/
---

## visitEditableRangeEnd(editableRangeEnd) {#editablerangeend}

Called when an end of an editable range is encountered in the document.


```js
visitEditableRangeEnd(editableRangeEnd: Aspose.Words.EditableRangeEnd)
```

| Parameter | Type | Description |
| --- | --- | --- |
| editableRangeEnd | [EditableRangeEnd](../../editablerangeend/) | The object that is being visited. |

### Returns

A [VisitorAction](../../visitoraction/) value that specifies how to continue the enumeration.


### Examples

Shows how to print the node structure of every editable range in a document.

```js
test('EditableRangeToText', () => {
  let doc = new aw.Document(base.myDir + "DocumentVisitor-compatible features.docx");
  let visitor = new EditableRangeStructurePrinter();

  // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
  // and then traverses all the node's children in a depth-first manner.
  // The visitor can read and modify each visited node.
  doc.accept(visitor);

  console.log(visitor.getText());
});


  /// <summary>
  /// Traverses a node's non-binary tree of child nodes.
  /// Creates a map in the form of a string of all encountered EditableRange nodes and their children.
  /// </summary>
public class EditableRangeStructurePrinter : DocumentVisitor
{
  public EditableRangeStructurePrinter()
  {
    mBuilder = new StringBuilder();
    mVisitorIsInsideEditableRange = false;
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
      // We want to print the contents of runs, but only if they are inside shapes, as they would be in the case of text boxes
    if (mVisitorIsInsideEditableRange) IndentAndAppendLine("[Run] \"" + run.getText() + "\"");

    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Called when an EditableRange node is encountered in the document.
    /// </summary>
  public override VisitorAction VisitEditableRangeStart(EditableRangeStart editableRangeStart)
  {
    IndentAndAppendLine("[EditableRange start] ID: " + editableRangeStart.id + " Owner: " +
              editableRangeStart.editableRange.singleUser);
    mDocTraversalDepth++;
    mVisitorIsInsideEditableRange = true;

    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Called when the visiting of a EditableRange node is ended.
    /// </summary>
  public override VisitorAction VisitEditableRangeEnd(EditableRangeEnd editableRangeEnd)
  {
    mDocTraversalDepth--;
    IndentAndAppendLine("[EditableRange end]");
    mVisitorIsInsideEditableRange = false;

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

  private bool mVisitorIsInsideEditableRange;
  private int mDocTraversalDepth;
  private readonly StringBuilder mBuilder;
}
```

### See Also

* module [Aspose.Words](../../)
* class [DocumentVisitor](../)

