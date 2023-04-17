---
title: Aspose::Words::EditableRange::Remove method
linktitle: Remove
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::EditableRange::Remove method. Removes the editable range from the document. Does not remove content inside the editable range in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words/editablerange/remove/
---
## EditableRange::Remove method


Removes the editable range from the document. Does not remove content inside the editable range.

```cpp
void Aspose::Words::EditableRange::Remove()
```


## Examples



Shows how to work with an editable range. 
```cpp
auto doc = MakeObject<Document>();
doc->Protect(ProtectionType::ReadOnly, u"MyPassword");

auto builder = MakeObject<DocumentBuilder>(doc);
builder->Writeln(String(u"Hello world! Since we have set the document's protection level to read-only,") +
                 u" we cannot edit this paragraph without the password.");

// Editable ranges allow us to leave parts of protected documents open for editing.
SharedPtr<EditableRangeStart> editableRangeStart = builder->StartEditableRange();
builder->Writeln(u"This paragraph is inside an editable range, and can be edited.");
SharedPtr<EditableRangeEnd> editableRangeEnd = builder->EndEditableRange();

// A well-formed editable range has a start node, and end node.
// These nodes have matching IDs and encompass editable nodes.
SharedPtr<EditableRange> editableRange = editableRangeStart->get_EditableRange();

ASSERT_EQ(editableRangeStart->get_Id(), editableRange->get_Id());
ASSERT_EQ(editableRangeEnd->get_Id(), editableRange->get_Id());

// Different parts of the editable range link to each other.
ASSERT_EQ(editableRangeStart->get_Id(), editableRange->get_EditableRangeStart()->get_Id());
ASSERT_EQ(editableRangeStart->get_Id(), editableRangeEnd->get_EditableRangeStart()->get_Id());
ASSERT_EQ(editableRange->get_Id(), editableRangeStart->get_EditableRange()->get_Id());
ASSERT_EQ(editableRangeEnd->get_Id(), editableRange->get_EditableRangeEnd()->get_Id());

// We can access the node types of each part like this. The editable range itself is not a node,
// but an entity which consists of a start, an end, and their enclosed contents.
ASSERT_EQ(NodeType::EditableRangeStart, editableRangeStart->get_NodeType());
ASSERT_EQ(NodeType::EditableRangeEnd, editableRangeEnd->get_NodeType());

builder->Writeln(u"This paragraph is outside the editable range, and cannot be edited.");

doc->Save(ArtifactsDir + u"EditableRange.CreateAndRemove.docx");

// Remove an editable range. All the nodes that were inside the range will remain intact.
editableRange->Remove();
```

## See Also

* Class [EditableRange](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
