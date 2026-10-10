---
title: "Aspose::Words::Layout::RevisionOptions::get_ShowOriginalRevision طريقة"
linktitle: "get_ShowOriginalRevision"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Layout::RevisionOptions::get_ShowOriginalRevision طريقة. يسمح بتحديد ما إذا كان يجب عرض النص الأصلي بدلاً من النص المعدل. القيمة الافتراضية هي false في C++."
type: docs
weight: 18000
url: /ar/cpp/aspose.words.layout/revisionoptions/get_showoriginalrevision/
---
## RevisionOptions::get_ShowOriginalRevision method


يسمح بتحديد ما إذا كان يجب إظهار النص الأصلي بدلاً من النص المُراجع. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Layout::RevisionOptions::get_ShowOriginalRevision() const
```


## أمثلة



يظهر كيفية تعديل مظهر المراجعات.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

// احصل على كائن RevisionOptions الذي يتحكم في مظهر المراجعات.
System::SharedPtr<Aspose::Words::Layout::RevisionOptions> revisionOptions = doc->get_LayoutOptions()->get_RevisionOptions();

// اعرض مراجعات الإدراج باللون الأخضر ومائلًا.
revisionOptions->set_InsertedTextColor(Aspose::Words::Layout::RevisionColor::Green);
revisionOptions->set_InsertedTextEffect(Aspose::Words::Layout::RevisionTextEffect::Italic);

// اعرض مراجعات الحذف باللون الأحمر وغامقًا.
revisionOptions->set_DeletedTextColor(Aspose::Words::Layout::RevisionColor::Red);
revisionOptions->set_DeletedTextEffect(Aspose::Words::Layout::RevisionTextEffect::Bold);

// سيظهر النص نفسه مرتين في مراجعة النقل:
// مرة عند نقطة الانطلاق ومرة عند وجهة الوصول.
// اعرض النص في مراجعة النقل من المصدر أصفر مع شطب مزدوج
// وزرقًا مسطرًا مزدوجًا في مراجعة النقل إلى الوجهة.
revisionOptions->set_MovedFromTextColor(Aspose::Words::Layout::RevisionColor::Yellow);
revisionOptions->set_MovedFromTextEffect(Aspose::Words::Layout::RevisionTextEffect::DoubleStrikeThrough);
revisionOptions->set_MovedToTextColor(Aspose::Words::Layout::RevisionColor::ClassicBlue);
revisionOptions->set_MovedToTextEffect(Aspose::Words::Layout::RevisionTextEffect::DoubleUnderline);

// اعرض مراجعات التنسيق باللون الأحمر الداكن وغامقًا.
revisionOptions->set_RevisedPropertiesColor(Aspose::Words::Layout::RevisionColor::DarkRed);
revisionOptions->set_RevisedPropertiesEffect(Aspose::Words::Layout::RevisionTextEffect::Bold);

// ضع شريطًا سميكًا أزرقًا داكنًا على الجانب الأيسر من الصفحة بجوار الأسطر المتأثرة بالمراجعات.
revisionOptions->set_RevisionBarsColor(Aspose::Words::Layout::RevisionColor::DarkBlue);
revisionOptions->set_RevisionBarsWidth(15.0f);

// اعرض علامات المراجعة والنص الأصلي.
revisionOptions->set_ShowOriginalRevision(true);
revisionOptions->set_ShowRevisionMarks(true);

// احصل على مراجعات النقل والحذف والتنسيق والتعليقات لتظهر في بالونات خضراء
// على الجانب الأيمن من الصفحة.
revisionOptions->set_ShowInBalloons(Aspose::Words::Layout::ShowInBalloons::Format);
revisionOptions->set_CommentColor(Aspose::Words::Layout::RevisionColor::BrightGreen);

// هذه الميزات تنطبق فقط على صيغ مثل .pdf أو .jpg.
doc->Save(get_ArtifactsDir() + u"Revision.RevisionOptions.pdf");
```

## انظر أيضًا

* Class [RevisionOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
