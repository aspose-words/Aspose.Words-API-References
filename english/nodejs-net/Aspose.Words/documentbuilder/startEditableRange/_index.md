---
title: DocumentBuilder.startEditableRange method
linktitle: startEditableRange method
articleTitle: startEditableRange method
second_title: Aspose.Words for Node.js
description: "DocumentBuilder.startEditableRange method. Marks the current position in the document as an editable range start."
type: docs
weight: 670
url: /nodejs-net/aspose.words/documentbuilder/startEditableRange/
---

## startEditableRange() {#default}

Marks the current position in the document as an editable range start.


```js
startEditableRange()
```

### Remarks

Editable range in a document can overlap and span any range. To create a valid editable range you need to
call both [DocumentBuilder.startEditableRange()](./#default) and [DocumentBuilder.endEditableRange()](../endEditableRange/#default)
or [DocumentBuilder.endEditableRange()](../endEditableRange/#editablerangestart) methods.

Badly formed editable range will be ignored when the document is saved.




### Returns

The editable range start node that was just created.


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

Shows how to create nested editable ranges.

```js
let doc = new aw.Document();
doc.protect(aw.ProtectionType.ReadOnly, "MyPassword");

let builder = new aw.DocumentBuilder(doc);
builder.writeln("Hello world! Since we have set the document's protection level to read-only, " +
        "we cannot edit this paragraph without the password.");

// Create two nested editable ranges.
let outerEditableRangeStart = builder.startEditableRange();
builder.writeln("This paragraph inside the outer editable range and can be edited.");

let innerEditableRangeStart = builder.startEditableRange();
builder.writeln("This paragraph inside both the outer and inner editable ranges and can be edited.");

// Currently, the document builder's node insertion cursor is in more than one ongoing editable range.
// When we want to end an editable range in this situation,
// we need to specify which of the ranges we wish to end by passing its EditableRangeStart node.
builder.endEditableRange(innerEditableRangeStart);

builder.writeln("This paragraph inside the outer editable range and can be edited.");

builder.endEditableRange(outerEditableRangeStart);

builder.writeln("This paragraph is outside any editable ranges, and cannot be edited.");

// If a region of text has two overlapping editable ranges with specified groups,
// the combined group of users excluded by both groups are prevented from editing it.
outerEditableRangeStart.editableRange.editorGroup = aw.EditorType.Everyone;
innerEditableRangeStart.editableRange.editorGroup = aw.EditorType.Contributors;

doc.save(base.artifactsDir + "EditableRange.Nested.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)

