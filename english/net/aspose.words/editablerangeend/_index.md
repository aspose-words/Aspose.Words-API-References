---
title: Class EditableRangeEnd
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.EditableRangeEnd class. Represents an end of an editable range in a Word document in C#.
type: docs
weight: 1280
url: /net/aspose.words/editablerangeend/
---
## EditableRangeEnd class

Represents an end of an editable range in a Word document.

To learn more, visit the [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) documentation article.

```csharp
public sealed class EditableRangeEnd : Node
```

## Properties

| Name | Description |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Specifies custom node identifier. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Gets the document to which this node belongs. |
| [EditableRangeStart](../../aspose.words/editablerangeend/editablerangestart/) { get; } | Corresponding [`EditableRangeStart`](../editablerangestart/), received by ID. |
| [Id](../../aspose.words/editablerangeend/id/) { get; set; } | Specifies the identifier of the editable range. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Returns `true` if this node can contain other nodes. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Gets the node immediately following this node. |
| override [NodeType](../../aspose.words/editablerangeend/nodetype/) { get; } | Returns EditableRangeEnd. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Gets the immediate parent of this node. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Gets the node immediately preceding this node. |
| [Range](../../aspose.words/node/range/) { get; } | Returns a [`Range`](../range/) object that represents the portion of a document that is contained in this node. |

## Methods

| Name | Description |
| --- | --- |
| override [Accept](../../aspose.words/editablerangeend/accept/)(DocumentVisitor) | Accepts a visitor. |
| [Clone](../../aspose.words/node/clone/)(bool) | Creates a duplicate of the node. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Gets the first ancestor of the specified [`NodeType`](../nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Gets the first ancestor of the specified object type. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Gets the text of this node and of all its children. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Gets next node according to the pre-order tree traversal algorithm. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../../aspose.words/node/remove/)() | Removes itself from the parent. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exports the content of the node into a string in the specified format. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exports the content of the node into a string using the specified save options. |

## Remarks

A complete editable range in a Word document consists of a [`EditableRangeStart`](./editablerangestart/) and a matching `EditableRangeEnd` with the same Id.

[`EditableRangeStart`](./editablerangestart/) and `EditableRangeEnd` are just markers inside a document that specify where the editable range starts and ends.

Use the [`EditableRange`](../editablerange/) class as a "facade" to work with an editable range as a single object.

Currently editable ranges are supported only at the inline-level, that is inside [`Paragraph`](../paragraph/), but editable range start and editable range end can be in different paragraphs.

## Examples

Shows how to limit the editing rights of editable ranges to a specific group/user.

```csharp
{
    Document doc = new Document();
    doc.Protect(ProtectionType.ReadOnly, "MyPassword");

    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                    " we cannot edit this paragraph without the password.");

    // When we write-protect documents, editable ranges allow us to pick specific areas that users may edit.
    // There are two mutually exclusive ways to narrow down the list of allowed editors.
    // 1 -  Specify a user:
    EditableRange editableRange = builder.StartEditableRange().EditableRange;
    editableRange.SingleUser = "john.doe@myoffice.com";
    builder.Writeln($"This paragraph is inside the first editable range, can only be edited by {editableRange.SingleUser}.");
    builder.EndEditableRange();

    Assert.AreEqual(EditorType.Unspecified, editableRange.EditorGroup);

    // 2 -  Specify a group that allowed users are associated with:
    editableRange = builder.StartEditableRange().EditableRange;
    editableRange.EditorGroup = EditorType.Administrators;
    builder.Writeln($"This paragraph is inside the first editable range, can only be edited by {editableRange.EditorGroup}.");
    builder.EndEditableRange();

    Assert.AreEqual(string.Empty, editableRange.SingleUser);

    builder.Writeln("This paragraph is outside the editable range, and cannot be edited by anybody.");

    // Print details and contents of every editable range in the document.
    EditableRangePrinter editableRangePrinter = new EditableRangePrinter();

    doc.Accept(editableRangePrinter);

    Console.WriteLine(editableRangePrinter.ToText());
}

/// <summary>
/// Collects properties and contents of visited editable ranges in a string.
/// </summary>
public class EditableRangePrinter : DocumentVisitor
{
    public EditableRangePrinter()
    {
        mBuilder = new StringBuilder();
    }

    public string ToText()
    {
        return mBuilder.ToString();
    }

    public void Reset()
    {
        mBuilder.Clear();
        mInsideEditableRange = false;
    }

    /// <summary>
    /// Called when an EditableRangeStart node is encountered in the document.
    /// </summary>
    public override VisitorAction VisitEditableRangeStart(EditableRangeStart editableRangeStart)
    {
        mBuilder.AppendLine(" -- Editable range found! -- ");
        mBuilder.AppendLine("\tID:\t\t" + editableRangeStart.Id);
        if (editableRangeStart.EditableRange.SingleUser == string.Empty)
            mBuilder.AppendLine("\tGroup:\t" + editableRangeStart.EditableRange.EditorGroup);
        else
            mBuilder.AppendLine("\tUser:\t" + editableRangeStart.EditableRange.SingleUser);
        mBuilder.AppendLine("\tContents:");

        mInsideEditableRange = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Called when an EditableRangeEnd node is encountered in the document.
    /// </summary>
    public override VisitorAction VisitEditableRangeEnd(EditableRangeEnd editableRangeEnd)
    {
        mBuilder.AppendLine(" -- End of editable range --\n");

        mInsideEditableRange = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Called when a Run node is encountered in the document. This visitor only records runs that are inside editable ranges.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mInsideEditableRange) mBuilder.AppendLine("\t\"" + run.Text + "\"");

        return VisitorAction.Continue;
    }

    private bool mInsideEditableRange;
    private readonly StringBuilder mBuilder;
}
```

### See Also

* class [Node](../node/)
* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
