---
title: EditableRange.editor_group property
linktitle: editor_group property
articleTitle: editor_group property
second_title: Aspose.Words for Python
description: "EditableRange.editor_group property. Returns or sets an alias (or editing group) which shall be used to determine if the current user shall be allowed to edit this editable range."
type: docs
weight: 30
url: /python-net/aspose.words/editablerange/editor_group/
---

## EditableRange.editor_group property

Returns or sets an alias (or editing group) which shall be used to determine if the current user
shall be allowed to edit this editable range.

Single user and editor group cannot be set simultaneously for the specific editable range,
if the one is set, the other will be clear.




### Examples

Shows how to create nested editable ranges.

```python
doc = aw.Document()
doc.protect(aw.ProtectionType.READ_ONLY, "MyPassword")

builder = aw.DocumentBuilder(doc)
builder.writeln("Hello world! Since we have set the document's protection level to read-only, " +
                "we cannot edit this paragraph without the password.")

# Create two nested editable ranges.
outer_editable_range_start = builder.start_editable_range()
builder.writeln("This paragraph inside the outer editable range and can be edited.")

inner_editable_range_start = builder.start_editable_range()
builder.writeln("This paragraph inside both the outer and inner editable ranges and can be edited.")

# Currently, the document builder's node insertion cursor is in more than one ongoing editable range.
# When we want to end an editable range in this situation,
# we need to specify which of the ranges we wish to end by passing its EditableRangeStart node.
builder.end_editable_range(inner_editable_range_start)

builder.writeln("This paragraph inside the outer editable range and can be edited.")

builder.end_editable_range(outer_editable_range_start)

builder.writeln("This paragraph is outside any editable ranges, and cannot be edited.")

# If a region of text has two overlapping editable ranges with specified groups,
# the combined group of users excluded by both groups are prevented from editing it.
outer_editable_range_start.editable_range.editor_group = aw.EditorType.EVERYONE
inner_editable_range_start.editable_range.editor_group = aw.EditorType.CONTRIBUTORS

doc.save(ARTIFACTS_DIR + "EditableRange.nested.docx")
```

### See Also

* module [aspose.words](../../)
* class [EditableRange](../)

