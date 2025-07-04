---
title: EditableRangeEnd.Id
linktitle: Id
articleTitle: Id
second_title: Aspose.Words for .NET
description: Discover the EditableRangeEnd Id property to easily identify and manage your editable ranges, enhancing your document's interactivity and control.
type: docs
weight: 20
url: /net/aspose.words/editablerangeend/id/
---
## EditableRangeEnd.Id property

Specifies the identifier of the editable range.

```csharp
public int Id { get; set; }
```

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

Assert.That(editableRange.Id, Is.EqualTo(editableRangeStart.Id));
Assert.That(editableRange.Id, Is.EqualTo(editableRangeEnd.Id));

// Different parts of the editable range link to each other.
Assert.That(editableRange.EditableRangeStart.Id, Is.EqualTo(editableRangeStart.Id));
Assert.That(editableRangeEnd.EditableRangeStart.Id, Is.EqualTo(editableRangeStart.Id));
Assert.That(editableRangeStart.EditableRange.Id, Is.EqualTo(editableRange.Id));
Assert.That(editableRange.EditableRangeEnd.Id, Is.EqualTo(editableRangeEnd.Id));

// We can access the node types of each part like this. The editable range itself is not a node,
// but an entity which consists of a start, an end, and their enclosed contents.
Assert.That(editableRangeStart.NodeType, Is.EqualTo(NodeType.EditableRangeStart));
Assert.That(editableRangeEnd.NodeType, Is.EqualTo(NodeType.EditableRangeEnd));

builder.Writeln("This paragraph is outside the editable range, and cannot be edited.");

doc.Save(ArtifactsDir + "EditableRange.CreateAndRemove.docx");

// Remove an editable range. All the nodes that were inside the range will remain intact.
editableRange.Remove();
```

### See Also

* class [EditableRangeEnd](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
