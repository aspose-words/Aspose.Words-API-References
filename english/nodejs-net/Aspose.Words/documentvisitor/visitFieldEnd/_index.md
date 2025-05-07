---
title: DocumentVisitor.visitFieldEnd method
linktitle: visitFieldEnd method
articleTitle: visitFieldEnd method
second_title: Aspose.Words for Node.js
description: "DocumentVisitor.visitFieldEnd method. Called when a field ends in the document."
type: docs
weight: 180
url: /nodejs-net/aspose.words/documentvisitor/visitFieldEnd/
---

## visitFieldEnd(fieldEnd) {#fieldend}

Called when a field ends in the document.


```js
visitFieldEnd(fieldEnd: Aspose.Words.Fields.FieldEnd)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fieldEnd | [FieldEnd](../../../aspose.words.fields/fieldend/) | The object that is being visited. |

### Remarks

For more info see [DocumentVisitor.visitFieldStart()](../visitFieldStart/#fieldstart)





### Returns

A [VisitorAction](../../visitoraction/) value that specifies how to continue the enumeration.


### Examples

Shows how to print the node structure of every field in a document.

```js
test('FieldToText', () => {
  let doc = new aw.Document(base.myDir + "DocumentVisitor-compatible features.docx");
  let visitor = new FieldStructurePrinter();

  // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
  // and then traverses all the node's children in a depth-first manner.
  // The visitor can read and modify each visited node.
  doc.accept(visitor);

  console.log(visitor.getText());
});


  /// <summary>
  /// Traverses a node's non-binary tree of child nodes.
  /// Creates a map in the form of a string of all encountered Field nodes and their children.
  /// </summary>
public class FieldStructurePrinter : DocumentVisitor
{
  public FieldStructurePrinter()
  {
    mBuilder = new StringBuilder();
    mVisitorIsInsideField = false;
  }

  public string GetText()
  {
    return mBuilder.toString();
  }

    /// <summary>
    /// Called when a Run node is encountered in the document.
    /// </summary>
  public override VisitorAction VisitRun(Run run)
  {
    if (mVisitorIsInsideField) IndentAndAppendLine("[Run] \"" + run.getText() + "\"");

    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Called when a FieldStart node is encountered in the document.
    /// </summary>
  public override VisitorAction VisitFieldStart(FieldStart fieldStart)
  {
    IndentAndAppendLine("[Field start] FieldType: " + fieldStart.fieldType);
    mDocTraversalDepth++;
    mVisitorIsInsideField = true;

    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Called when a FieldEnd node is encountered in the document.
    /// </summary>
  public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
  {
    mDocTraversalDepth--;
    IndentAndAppendLine("[Field end]");
    mVisitorIsInsideField = false;

    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Called when a FieldSeparator node is encountered in the document.
    /// </summary>
  public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
  {
    IndentAndAppendLine("[FieldSeparator]");

    return aw.VisitorAction.Continue;
  }

    /// <summary>
    /// Append a line to the StringBuilder, and indent it depending on how deep the visitor is
    /// into the field's tree of child nodes.
    /// </summary>
    /// <param name="text"></param>
  private void IndentAndAppendLine(string text)
  {
    for (let i = 0; i < mDocTraversalDepth; i++)
    {
      mBuilder.append("|  ");
    }

    mBuilder.AppendLine(text);
  }

  private bool mVisitorIsInsideField;
  private int mDocTraversalDepth;
  private readonly StringBuilder mBuilder;
}
```

### See Also

* module [Aspose.Words](../../)
* class [DocumentVisitor](../)

