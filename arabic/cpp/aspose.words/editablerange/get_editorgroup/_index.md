---
title: "طريقة Aspose::Words::EditableRange::get_EditorGroup"
linktitle: "get_EditorGroup"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::EditableRange::get_EditorGroup. تُعيد أو تُعيّن اسمًا مستعارًا (أو مجموعة تحرير) يُستخدم لتحديد ما إذا كان يُسمح للمستخدم الحالي بتحرير هذا النطاق القابل للتحرير في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words/editablerange/get_editorgroup/
---
## EditableRange::get_EditorGroup method


يعيد أو يضبط اسمًا مستعارًا (أو مجموعة تحرير) يُستخدم لتحديد ما إذا كان يُسمح للمستخدم الحالي بتحرير هذا النطاق القابل للتحرير.

```cpp
Aspose::Words::EditorType Aspose::Words::EditableRange::get_EditorGroup()
```

## ملاحظات


لا يمكن تعيين المستخدم الفردي ومجموعة المحرر في نفس الوقت للنطاق القابل للتحرير المحدد؛ إذا تم تعيين أحدهما، سيُمسح الآخر.

## أمثلة



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

* Enum [EditorType](../../editortype/)
* Class [EditableRange](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
