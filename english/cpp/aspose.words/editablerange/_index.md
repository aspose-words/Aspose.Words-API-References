---
title: Aspose::Words::EditableRange class
linktitle: EditableRange
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::EditableRange class. Represents a single editable range. To learn more, visit the  documentation article in C++.'
type: docs
weight: 24000
url: /cpp/aspose.words/editablerange/
---
## EditableRange class


Represents a single editable range. To learn more, visit the [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) documentation article.

```cpp
class EditableRange : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_EditableRangeEnd](./get_editablerangeend/)() | Gets the node that represents the end of the editable range. |
| [get_EditableRangeStart](./get_editablerangestart/)() const | Gets the node that represents the start of the editable range. |
| [get_EditorGroup](./get_editorgroup/)() | Returns or sets an alias (or editing group) which shall be used to determine if the current user shall be allowed to edit this editable range. |
| [get_Id](./get_id/)() | Gets the editable range identifier. |
| [get_SingleUser](./get_singleuser/)() | Returns or sets the single user for editable range. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Removes the editable range from the document. Does not remove content inside the editable range. |
| [set_EditorGroup](./set_editorgroup/)(Aspose::Words::EditorType) | Setter for [Aspose::Words::EditableRange::get_EditorGroup](./get_editorgroup/). |
| [set_SingleUser](./set_singleuser/)(const System::String\&) | Setter for [Aspose::Words::EditableRange::get_SingleUser](./get_singleuser/). |
| static [Type](./type/)() |  |
## Remarks


[EditableRange](./) is a "facade" object that encapsulates two nodes [EditableRangeStart](./get_editablerangestart/) and [EditableRangeEnd](./get_editablerangeend/) in a document tree and allows to work with an editable range as a single object.

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
