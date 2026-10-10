---
title: "طريقة Aspose::Words::DocumentBuilder::StartEditableRange"
linktitle: "StartEditableRange"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::DocumentBuilder::StartEditableRange. تُحدد الموضع الحالي في المستند كبداية نطاق قابل للتحرير بلغة C++."
type: docs
weight: 70000
url: /ar/cpp/aspose.words/documentbuilder/starteditablerange/
---
## DocumentBuilder::StartEditableRange method


يحدد الموضع الحالي في المستند كبداية نطاق قابل للتحرير.

```cpp
System::SharedPtr<Aspose::Words::EditableRangeStart> Aspose::Words::DocumentBuilder::StartEditableRange()
```


### ReturnValue

عقدة بداية النطاق القابل للتحرير التي تم إنشاؤها للتو.
## ملاحظات


يمكن أن يتداخل النطاق القابل للتحرير في المستند ويغطي أي نطاق. لإنشاء نطاق قابل للتحرير صالح، تحتاج إلى استدعاء كل من [StartEditableRange](./) و[EndEditableRange](../endeditablerange/) أو [EndEditableRange()](../).

سيتم تجاهل النطاق القابل للتحرير غير المُشكل بشكل صحيح عند حفظ المستند.

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


يُظهر كيفية إنشاء نطاقات تحرير متداخلة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
doc->Protect(Aspose::Words::ProtectionType::ReadOnly, u"MyPassword");

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(System::String(u"Hello world! Since we have set the document's protection level to read-only, ") + u"we cannot edit this paragraph without the password.");

// إنشاء نطاقين تحرير متداخلين.
System::SharedPtr<Aspose::Words::EditableRangeStart> outerEditableRangeStart = builder->StartEditableRange();
builder->Writeln(u"This paragraph inside the outer editable range and can be edited.");

System::SharedPtr<Aspose::Words::EditableRangeStart> innerEditableRangeStart = builder->StartEditableRange();
builder->Writeln(u"This paragraph inside both the outer and inner editable ranges and can be edited.");

// حاليًا، مؤشر إدراج العقدة في مُنشئ المستند موجود في أكثر من نطاق تحرير جارٍ.
// عند رغبتنا في إنهاء نطاق تحرير في هذا الوضع،
// نحتاج إلى تحديد أي من النطاقات نريد إنهاؤه بتمرير عقدة EditableRangeStart الخاصة به.
builder->EndEditableRange(innerEditableRangeStart);

builder->Writeln(u"This paragraph inside the outer editable range and can be edited.");

builder->EndEditableRange(outerEditableRangeStart);

builder->Writeln(u"This paragraph is outside any editable ranges, and cannot be edited.");

// إذا كان جزء من النص يحتوي على نطاقين تحرير متداخلين مع مجموعات محددة،
// فإن مجموعة المستخدمين المستبعدة من كلا المجموعتين معًا تُمنع من تحريره.
outerEditableRangeStart->get_EditableRange()->set_EditorGroup(Aspose::Words::EditorType::Everyone);
innerEditableRangeStart->get_EditableRange()->set_EditorGroup(Aspose::Words::EditorType::Contributors);

doc->Save(get_ArtifactsDir() + u"EditableRange.Nested.docx");
```

## انظر أيضًا

* Class [EditableRangeStart](../../editablerangestart/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
