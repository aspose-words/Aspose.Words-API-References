---
title: Aspose::Words::EditableRangeEnd::get_NodeType method
linktitle: get_NodeType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::EditableRangeEnd::get_NodeType method. Returns EditableRangeEnd in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words/editablerangeend/get_nodetype/
---
## EditableRangeEnd::get_NodeType method


Returns [EditableRangeEnd](../../nodetype/).

```cpp
Aspose::Words::NodeType Aspose::Words::EditableRangeEnd::get_NodeType() const override
```


## Examples



Shows how to work with an editable range. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
doc->Protect(Aspose::Words::ProtectionType::ReadOnly, u"MyPassword");

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(System::String(u"Hello world! Since we have set the document's protection level to read-only,") + u" we cannot edit this paragraph without the password.");

// Editable ranges allow us to leave parts of protected documents open for editing.
System::SharedPtr<Aspose::Words::EditableRangeStart> editableRangeStart = builder->StartEditableRange();
builder->Writeln(u"This paragraph is inside an editable range, and can be edited.");
System::SharedPtr<Aspose::Words::EditableRangeEnd> editableRangeEnd = builder->EndEditableRange();

// A well-formed editable range has a start node, and end node.
// These nodes have matching IDs and encompass editable nodes.
System::SharedPtr<Aspose::Words::EditableRange> editableRange = editableRangeStart->get_EditableRange();

ASSERT_EQ(editableRangeStart->get_Id(), editableRange->get_Id());
ASSERT_EQ(editableRangeEnd->get_Id(), editableRange->get_Id());

// Different parts of the editable range link to each other.
ASSERT_EQ(editableRangeStart->get_Id(), editableRange->get_EditableRangeStart()->get_Id());
ASSERT_EQ(editableRangeStart->get_Id(), editableRangeEnd->get_EditableRangeStart()->get_Id());
ASSERT_EQ(editableRange->get_Id(), editableRangeStart->get_EditableRange()->get_Id());
ASSERT_EQ(editableRangeEnd->get_Id(), editableRange->get_EditableRangeEnd()->get_Id());

// We can access the node types of each part like this. The editable range itself is not a node,
// but an entity which consists of a start, an end, and their enclosed contents.
ASSERT_EQ(Aspose::Words::NodeType::EditableRangeStart, editableRangeStart->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::EditableRangeEnd, editableRangeEnd->get_NodeType());

builder->Writeln(u"This paragraph is outside the editable range, and cannot be edited.");

doc->Save(get_ArtifactsDir() + u"EditableRange.CreateAndRemove.docx");

// Remove an editable range. All the nodes that were inside the range will remain intact.
editableRange->Remove();
```

## See Also

* Enum [NodeType](../../nodetype/)
* Class [EditableRangeEnd](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
