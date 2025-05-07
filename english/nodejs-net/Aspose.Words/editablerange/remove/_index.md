---
title: EditableRange.remove method
linktitle: remove method
articleTitle: remove method
second_title: Aspose.Words for Node.js
description: "EditableRange.remove method. Removes the editable range from the document"
type: docs
weight: 60
url: /nodejs-net/aspose.words/editablerange/remove/
---

## remove() {#default}

Removes the editable range from the document. Does not remove content inside the editable range.


```js
remove()
```

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

* module [Aspose.Words](../../)
* class [EditableRange](../)

