---
title: Aspose::Words::EditableRange::get_EditorGroup method
linktitle: get_EditorGroup
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::EditableRange::get_EditorGroup method. Returns or sets an alias (or editing group) which shall be used to determine if the current user shall be allowed to edit this editable range in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words/editablerange/get_editorgroup/
---
## EditableRange::get_EditorGroup method


Returns or sets an alias (or editing group) which shall be used to determine if the current user shall be allowed to edit this editable range.

```cpp
Aspose::Words::EditorType Aspose::Words::EditableRange::get_EditorGroup()
```

## Remarks


Single user and editor group cannot be set simultaneously for the specific editable range, if the one is set, the other will be clear.

## Examples



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

* Enum [EditorType](../../editortype/)
* Class [EditableRange](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
