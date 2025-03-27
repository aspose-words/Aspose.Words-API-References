---
title: DocumentBuilder.endEditableRange method
linktitle: endEditableRange method
articleTitle: endEditableRange method
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.DocumentBuilder.endEditableRange method"
type: docs
weight: 230
url: /nodejs-net/Aspose.Words/documentbuilder/endEditableRange/
---

## endEditableRange() {#default}

Marks the current position in the document as an editable range end.


```js
endEditableRange()
```

### Remarks

Editable range in a document can overlap and span any range. To create a valid editable range you need to
call both [DocumentBuilder.startEditableRange()](../startEditableRange/#default) and [DocumentBuilder.endEditableRange()](./#default)
or [DocumentBuilder.endEditableRange()](./#editablerangestart) methods.

Badly formed editable range will be ignored when the document is saved.




### Returns

The editable range end node that was just created.


## endEditableRange(start) {#editablerangestart}

Marks the current position in the document as an editable range end.


```js
endEditableRange(start: Aspose.Words.EditableRangeStart)
```

| Parameter | Type | Description |
| --- | --- | --- |
| start | [EditableRangeStart](../../editablerangestart/) | This editable range start. |

### Remarks

Use this overload during creating nested editable ranges.

Editable range in a document can overlap and span any range. To create a valid editable range you need to
call both [DocumentBuilder.startEditableRange()](../startEditableRange/#default) and [DocumentBuilder.endEditableRange()](./#default)
or [DocumentBuilder.endEditableRange()](./#editablerangestart) methods.

Badly formed editable range will be ignored when the document is saved.




### Returns

The editable range end node that was just created.


## Examples

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

## See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)

