---
title: "طريقة Aspose::Words::EditableRangeStart::get_NodeType"
linktitle: "get_NodeType"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::EditableRangeStart::get_NodeType. تُرجع EditableRangeStart في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words/editablerangestart/get_nodetype/
---
## EditableRangeStart::get_NodeType method


تُرجع [EditableRangeStart](../../nodetype/).

```cpp
Aspose::Words::NodeType Aspose::Words::EditableRangeStart::get_NodeType() const override
```


## أمثلة



يوضح كيفية العمل مع نطاق قابل للتحرير.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
doc->Protect(Aspose::Words::ProtectionType::ReadOnly, u"MyPassword");

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(System::String(u"Hello world! Since we have set the document's protection level to read-only,") + u" we cannot edit this paragraph without the password.");

// تسمح النطاقات القابلة للتحرير بترك أجزاء من المستندات المحمية مفتوحة للتحرير.
System::SharedPtr<Aspose::Words::EditableRangeStart> editableRangeStart = builder->StartEditableRange();
builder->Writeln(u"This paragraph is inside an editable range, and can be edited.");
System::SharedPtr<Aspose::Words::EditableRangeEnd> editableRangeEnd = builder->EndEditableRange();

// النطاق القابل للتحرير المُشكل بشكل صحيح يحتوي على عقدة بداية وعقدة نهاية.
// هذه العقد لها معرّفات متطابقة وتضمّن عقد قابلة للتحرير.
System::SharedPtr<Aspose::Words::EditableRange> editableRange = editableRangeStart->get_EditableRange();

ASSERT_EQ(editableRangeStart->get_Id(), editableRange->get_Id());
ASSERT_EQ(editableRangeEnd->get_Id(), editableRange->get_Id());

// أجزاء مختلفة من النطاق القابل للتحرير ترتبط ببعضها البعض.
ASSERT_EQ(editableRangeStart->get_Id(), editableRange->get_EditableRangeStart()->get_Id());
ASSERT_EQ(editableRangeStart->get_Id(), editableRangeEnd->get_EditableRangeStart()->get_Id());
ASSERT_EQ(editableRange->get_Id(), editableRangeStart->get_EditableRange()->get_Id());
ASSERT_EQ(editableRangeEnd->get_Id(), editableRange->get_EditableRangeEnd()->get_Id());

// يمكننا الوصول إلى أنواع العقد لكل جزء بهذه الطريقة. النطاق القابل للتحرير نفسه ليس عقدة،
// بل هو كيان يتكوّن من بداية ونهاية ومحتواهما المغلق.
ASSERT_EQ(Aspose::Words::NodeType::EditableRangeStart, editableRangeStart->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::EditableRangeEnd, editableRangeEnd->get_NodeType());

builder->Writeln(u"This paragraph is outside the editable range, and cannot be edited.");

doc->Save(get_ArtifactsDir() + u"EditableRange.CreateAndRemove.docx");

// إزالة نطاق قابل للتحرير. جميع العقد التي كانت داخل النطاق ستبقى سليمة.
editableRange->Remove();
```

## انظر أيضًا

* Enum [NodeType](../../nodetype/)
* Class [EditableRangeStart](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
