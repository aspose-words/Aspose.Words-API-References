---
title: EndEditableRange
second_title: Aspose.Words for C++ API Reference
description: Marks the current position in the document as an editable range end.
type: docs
weight: 53
url: /cpp/aspose.words/documentbuilder/endeditablerange/
---
## DocumentBuilder::EndEditableRange() method


Marks the current position in the document as an editable range end.

```cpp
System::SharedPtr<Aspose::Words::EditableRangeEnd> Aspose::Words::DocumentBuilder::EndEditableRange()
```


### ReturnValue

The editable range end node that was just created.
## Remarks


Editable range in a document can overlap and span any range. To create a valid editable range you need to call both [StartEditableRange](../starteditablerange/) and [EndEditableRange](./) or [EndEditableRange()](../) methods.

Badly formed editable range will be ignored when the document is saved.

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

* Class [EditableRangeEnd](../../editablerangeend/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
## DocumentBuilder::EndEditableRange(const System::SharedPtr\<Aspose::Words::EditableRangeStart\>\&) method


Marks the current position in the document as an editable range end.

```cpp
System::SharedPtr<Aspose::Words::EditableRangeEnd> Aspose::Words::DocumentBuilder::EndEditableRange(const System::SharedPtr<Aspose::Words::EditableRangeStart> &start)
```


| Parameter | Type | Description |
| --- | --- | --- |
| start | const System::SharedPtr\<Aspose::Words::EditableRangeStart\>\& | This editable range start. |

### ReturnValue

The editable range end node that was just created.
## Remarks


Use this overload during creating nested editable ranges.

Editable range in a document can overlap and span any range. To create a valid editable range you need to call both [StartEditableRange](../starteditablerange/) and [EndEditableRange](./) or [EndEditableRange()](../) methods.

Badly formed editable range will be ignored when the document is saved.

## Examples



Shows how to create nested editable ranges. 
```cpp
auto doc = MakeObject<Document>();
doc->Protect(ProtectionType::ReadOnly, u"MyPassword");

auto builder = MakeObject<DocumentBuilder>(doc);
builder->Writeln(String(u"Hello world! Since we have set the document's protection level to read-only, ") +
                 u"we cannot edit this paragraph without the password.");

// Create two nested editable ranges.
SharedPtr<EditableRangeStart> outerEditableRangeStart = builder->StartEditableRange();
builder->Writeln(u"This paragraph inside the outer editable range and can be edited.");

SharedPtr<EditableRangeStart> innerEditableRangeStart = builder->StartEditableRange();
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
outerEditableRangeStart->get_EditableRange()->set_EditorGroup(EditorType::Everyone);
innerEditableRangeStart->get_EditableRange()->set_EditorGroup(EditorType::Contributors);

doc->Save(ArtifactsDir + u"EditableRange.Nested.docx");
```

## See Also

* Class [EditableRangeEnd](../../editablerangeend/)
* Class [EditableRangeStart](../../editablerangestart/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
