---
title: "Aspose::Words::EditableRange class"
linktitle: "EditableRange"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::EditableRange. تمثل نطاقًا قابلًا للتحرير واحدًا. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 24000
url: /ar/cpp/aspose.words/editablerange/
---
## EditableRange class


يمثل نطاقًا قابلًا للتحرير واحدًا. لمعرفة المزيد، قم بزيارة مقالة الوثائق [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class EditableRange : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_EditableRangeEnd](./get_editablerangeend/)() | يحصل على العقدة التي تمثل نهاية النطاق القابل للتحرير. |
| [get_EditableRangeStart](./get_editablerangestart/)() const | يحصل على العقدة التي تمثل بداية النطاق القابل للتحرير. |
| [get_EditorGroup](./get_editorgroup/)() | يعيد أو يضبط اسمًا مستعارًا (أو مجموعة تحرير) يُستخدم لتحديد ما إذا كان يُسمح للمستخدم الحالي بتحرير هذا النطاق القابل للتحرير. |
| [get_Id](./get_id/)() | يحصل على معرف النطاق القابل للتحرير. |
| [get_SingleUser](./get_singleuser/)() | يعيد أو يضبط المستخدم الفردي للنطاق القابل للتحرير. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | يزيل النطاق القابل للتحرير من المستند. لا يزيل المحتوى داخل النطاق القابل للتحرير. |
| [set_EditorGroup](./set_editorgroup/)(Aspose::Words::EditorType) | مُعيّن لـ [Aspose::Words::EditableRange::get_EditorGroup](./get_editorgroup/). |
| [set_SingleUser](./set_singleuser/)(const System::String\&) | مُعيّن لـ [Aspose::Words::EditableRange::get_SingleUser](./get_singleuser/). |
| static [Type](./type/)() |  |
## ملاحظات


[EditableRange](./) is a "facade" object that encapsulates two nodes [EditableRangeStart](./get_editablerangestart/) and [EditableRangeEnd](./get_editablerangeend/) in a document tree and allows to work with an editable range as a single object.

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
