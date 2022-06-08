---
title: EditableRange
second_title: Aspose.Words for .NET API Reference
description: Represents a single editable range.
type: docs
weight: 1250
url: /net/aspose.words/editablerange/
---
## EditableRange class

Represents a single editable range.

```csharp
public class EditableRange
```

## Properties

| Name | Description |
| --- | --- |
| [EditableRangeEnd](../../aspose.words/editablerange/editablerangeend) { get; } | Gets the node that represents the end of the editable range. |
| [EditableRangeStart](../../aspose.words/editablerange/editablerangestart) { get; } | Gets the node that represents the start of the editable range. |
| [EditorGroup](../../aspose.words/editablerange/editorgroup) { get; set; } | Returns or sets an alias (or editing group) which shall be used to determine if the current user shall be allowed to edit this editable range. |
| [Id](../../aspose.words/editablerange/id) { get; } | Gets the editable range identifier. |
| [SingleUser](../../aspose.words/editablerange/singleuser) { get; set; } | Returns or sets the single user for editable range. |

## Methods

| Name | Description |
| --- | --- |
| [Remove](../../aspose.words/editablerange/remove)() | Removes the editable range from the document. Does not remove content inside the editable range. |

## Remarks

[`EditableRange`](../editablerange) is a "facade" object that encapsulates two nodes [`EditableRangeStart`](./editablerangestart) and [`EditableRangeEnd`](./editablerangeend) in a document tree and allows to work with an editable range as a single object.

## Examples

Shows how to work with an editable range.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "MyPassword");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                " we cannot edit this paragraph without the password.");

// Editable ranges allow us to leave parts of protected documents open for editing.
EditableRangeStart editableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph is inside an editable range, and can be edited.");
EditableRangeEnd editableRangeEnd = builder.EndEditableRange();

// A well-formed editable range has a start node, and end node.
// These nodes have matching IDs and encompass editable nodes.
EditableRange editableRange = editableRangeStart.EditableRange;

Assert.AreEqual(editableRangeStart.Id, editableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.Id);

// Different parts of the editable range link to each other.
Assert.AreEqual(editableRangeStart.Id, editableRange.EditableRangeStart.Id);
Assert.AreEqual(editableRangeStart.Id, editableRangeEnd.EditableRangeStart.Id);
Assert.AreEqual(editableRange.Id, editableRangeStart.EditableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.EditableRangeEnd.Id);

// We can access the node types of each part like this. The editable range itself is not a node,
// but an entity which consists of a start, an end, and their enclosed contents.
Assert.AreEqual(NodeType.EditableRangeStart, editableRangeStart.NodeType);
Assert.AreEqual(NodeType.EditableRangeEnd, editableRangeEnd.NodeType);

builder.Writeln("This paragraph is outside the editable range, and cannot be edited.");

doc.Save(ArtifactsDir + "EditableRange.CreateAndRemove.docx");

// Remove an editable range. All the nodes that were inside the range will remain intact.
editableRange.Remove();
```

Shows how to limit the editing rights of editable ranges to a specific group/user.

```csharp
public void Visitor()
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

* namespace [Aspose.Words](../../aspose.words)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
