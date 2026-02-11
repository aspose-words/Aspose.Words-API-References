---
title: EditableRange class
linktitle: EditableRange class
articleTitle: EditableRange class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.EditableRange class. Represents a single editable range"
type: docs
weight: 370
url: /nodejs-net/aspose.words/editablerange/
---

## EditableRange class

Represents a single editable range.
To learn more, visit the [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/nodejs-net/aspose-words-document-object-model/) documentation article.




### Remarks

[EditableRange](./) is a "facade" object that encapsulates two nodes [EditableRange.editableRangeStart](./editableRangeStart/)
and [EditableRange.editableRangeEnd](./editableRangeEnd/) in a document tree and allows to work with an editable range as a single object.




### Properties

| Name | Description |
| --- | --- |
| [editableRangeEnd](./editableRangeEnd/) | Gets the node that represents the end of the editable range. |
| [editableRangeStart](./editableRangeStart/) | Gets the node that represents the start of the editable range. |
| [editorGroup](./editorGroup/) | Returns or sets an alias (or editing group) which shall be used to determine if the current user shall be allowed to edit this editable range. |
| [id](./id/) | Gets the editable range identifier. |
| [singleUser](./singleUser/) | Returns or sets the single user for editable range. |

### Methods

| Name | Description |
| --- | --- |
|[ remove()](./remove/#default) | Removes the editable range from the document. Does not remove content inside the editable range. |

### Examples

Shows how to work with an editable range.

```js
let doc = new aw.Document();
doc.protect(aw.ProtectionType.ReadOnly, "MyPassword");

let builder = new aw.DocumentBuilder(doc);
builder.writeln("Hello world! Since we have set the document's protection level to read-only," +
        " we cannot edit this paragraph without the password.");

// Editable ranges allow us to leave parts of protected documents open for editing.
let editableRangeStart = builder.startEditableRange();
builder.writeln("This paragraph is inside an editable range, and can be edited.");
let editableRangeEnd = builder.endEditableRange();

// A well-formed editable range has a start node, and end node.
// These nodes have matching IDs and encompass editable nodes.
let editableRange = editableRangeStart.editableRange;

expect(editableRange.id).toEqual(editableRangeStart.id);
expect(editableRange.id).toEqual(editableRangeEnd.id);

// Different parts of the editable range link to each other.
expect(editableRange.editableRangeStart.id).toEqual(editableRangeStart.id);
expect(editableRangeEnd.editableRangeStart.id).toEqual(editableRangeStart.id);
expect(editableRangeStart.editableRange.id).toEqual(editableRange.id);
expect(editableRange.editableRangeEnd.id).toEqual(editableRangeEnd.id);

// We can access the node types of each part like this. The editable range itself is not a node,
// but an entity which consists of a start, an end, and their enclosed contents.
expect(editableRangeStart.nodeType).toEqual(aw.NodeType.EditableRangeStart);
expect(editableRangeEnd.nodeType).toEqual(aw.NodeType.EditableRangeEnd);

builder.writeln("This paragraph is outside the editable range, and cannot be edited.");

doc.save(base.artifactsDir + "EditableRange.CreateAndRemove.docx");

// Remove an editable range. All the nodes that were inside the range will remain intact.
editableRange.remove();
```

### See Also

* module [Aspose.Words](../)

