---
title: DocumentVisitor.VisitEditableRangeEnd
linktitle: VisitEditableRangeEnd
articleTitle: VisitEditableRangeEnd
second_title: Aspose.Words for .NET
description: Discover the DocumentVisitor VisitEditableRangeEnd method—efficiently handle editable range ends in your documents for seamless editing and enhanced functionality.
type: docs
weight: 160
url: /net/aspose.words/documentvisitor/visiteditablerangeend/
---
## DocumentVisitor.VisitEditableRangeEnd method

Called when an end of an editable range is encountered in the document.

```csharp
public virtual VisitorAction VisitEditableRangeEnd(EditableRangeEnd editableRangeEnd)
```

| Parameter | Type | Description |
| --- | --- | --- |
| editableRangeEnd | EditableRangeEnd | The object that is being visited. |

### Return Value

A [`VisitorAction`](../../visitoraction/) value that specifies how to continue the enumeration.

## Examples

Shows how to print the node structure of every editable range in a document.

```csharp
public void EditableRangeToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    EditableRangeStructurePrinter visitor = new EditableRangeStructurePrinter();

    // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
    // and then traverses all the node's children in a depth-first manner.
    // The visitor can read and modify each visited node.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

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
        return mBuilder.ToString();
    }

    /// <summary>
    /// Called when a Run node is encountered in the document.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        // We want to print the contents of runs, but only if they are inside shapes, as they would be in the case of text boxes
        if (mVisitorIsInsideEditableRange) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Called when an EditableRange node is encountered in the document.
    /// </summary>
    public override VisitorAction VisitEditableRangeStart(EditableRangeStart editableRangeStart)
    {
        IndentAndAppendLine("[EditableRange start] ID: " + editableRangeStart.Id + " Owner: " +
                            editableRangeStart.EditableRange.SingleUser);
        mDocTraversalDepth++;
        mVisitorIsInsideEditableRange = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Called when the visiting of a EditableRange node is ended.
    /// </summary>
    public override VisitorAction VisitEditableRangeEnd(EditableRangeEnd editableRangeEnd)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[EditableRange end]");
        mVisitorIsInsideEditableRange = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
    /// </summary>
    /// <param name="text"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++) mBuilder.Append("|  ");

        mBuilder.AppendLine(text);
    }

    private bool mVisitorIsInsideEditableRange;
    private int mDocTraversalDepth;
    private readonly StringBuilder mBuilder;
}
```

### See Also

* enum [VisitorAction](../../visitoraction/)
* class [EditableRangeEnd](../../editablerangeend/)
* class [DocumentVisitor](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
