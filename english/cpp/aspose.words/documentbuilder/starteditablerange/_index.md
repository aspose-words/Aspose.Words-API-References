---
title: Aspose::Words::DocumentBuilder::StartEditableRange method
linktitle: StartEditableRange
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentBuilder::StartEditableRange method. Marks the current position in the document as an editable range start in C++.'
type: docs
weight: 70000
url: /cpp/aspose.words/documentbuilder/starteditablerange/
---
## DocumentBuilder::StartEditableRange method


Marks the current position in the document as an editable range start.

```cpp
System::SharedPtr<Aspose::Words::EditableRangeStart> Aspose::Words::DocumentBuilder::StartEditableRange()
```


### ReturnValue

The editable range start node that was just created.
## Remarks


Editable range in a document can overlap and span any range. To create a valid editable range you need to call both [StartEditableRange](./) and [EndEditableRange](../endeditablerange/) or [EndEditableRange()](../) methods.

Badly formed editable range will be ignored when the document is saved.

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


Shows how to create nested editable ranges. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
doc->Protect(Aspose::Words::ProtectionType::ReadOnly, u"MyPassword");

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(System::String(u"Hello world! Since we have set the document's protection level to read-only, ") + u"we cannot edit this paragraph without the password.");

// Create two nested editable ranges.
System::SharedPtr<Aspose::Words::EditableRangeStart> outerEditableRangeStart = builder->StartEditableRange();
builder->Writeln(u"This paragraph inside the outer editable range and can be edited.");

System::SharedPtr<Aspose::Words::EditableRangeStart> innerEditableRangeStart = builder->StartEditableRange();
builder->Writeln(u"This paragraph inside both the outer and inner editable ranges and can be edited.");

// Currently, the document builder's node insertion cursor is in more than one ongoing editable range.
// When we want to end an editable range in this situation,
// we need to specify which of the ranges we wish to end by passing its EditableRangeStart node.
builder->EndEditableRange(innerEditableRangeStart);

builder->Writeln(u"This paragraph inside the outer editable range and can be edited.");

builder->EndEditableRange(outerEditableRangeStart);

builder->Writeln(u"This paragraph is outside any editable ranges, and cannot be edited.");

// If a region of text has two overlapping editable ranges with specified groups,
// the combined group of users excluded by both groups are prevented from editing it.
outerEditableRangeStart->get_EditableRange()->set_EditorGroup(Aspose::Words::EditorType::Everyone);
innerEditableRangeStart->get_EditableRange()->set_EditorGroup(Aspose::Words::EditorType::Contributors);

doc->Save(get_ArtifactsDir() + u"EditableRange.Nested.docx");
```

## See Also

* Class [EditableRangeStart](../../editablerangestart/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
