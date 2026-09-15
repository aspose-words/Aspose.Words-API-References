---
title: "Aspose::Words::Notes::FootnotePosition enum"
linktitle: "موضع الحاشية السفلية"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Notes::FootnotePosition enum. يحدد موضع الحاشية السفلية في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.notes/footnoteposition/
---
## FootnotePosition enum


يحدد موضع الحاشية السفلية.

```cpp
enum class FootnotePosition
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| BottomOfPage | 1 | يتم إخراج الحواشي السفلية في أسفل كل صفحة. |
| BeneathText | 2 | يتم إخراج الحواشي السفلية تحت النص في كل صفحة. |


## أمثلة



يعرض كيفية اختيار مكان مختلف حيث يجمع المستند ويعرض الحواشي الخاصة به.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// الحاشية هي طريقة لإرفاق مرجع أو تعليق جانبي بالنص
// الذي لا يتداخل مع تدفق نص الجسم الرئيسي.
// إدراج حاشية يضيف رمز مرجع صغير مرتفع
// في نص الجسم الرئيسي حيث نقوم بإدراج الحاشية.
// كل حاشية تنشئ أيضًا مدخلاً في أسفل الصفحة، يتكون من رمز
// يتطابق مع رمز الإشارة في نص الجسم الرئيسي.
// نص المرجع الذي نمرره إلى طريقة "InsertFootnote" في مُنشئ المستند.
builder->Write(u"Hello world!");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote contents.");

// يمكننا استخدام الخاصية "Position" لتحديد المكان الذي سيضع فيه المستند جميع حواشيه.
// إذا قمنا بتعيين قيمة الخاصية "Position" إلى "FootnotePosition.BottomOfPage",
// ستظهر كل حاشية في أسفل الصفحة التي تحتوي على علامة مرجعها. هذه هي القيمة الافتراضية.
// إذا قمنا بتعيين قيمة الخاصية "Position" إلى "FootnotePosition.BeneathText",
// ستظهر كل حاشية في نهاية نص الصفحة الذي يحتوي على علامة مرجعها.
doc->get_FootnoteOptions()->set_Position(footnotePosition);

doc->Save(get_ArtifactsDir() + u"InlineStory.PositionFootnote.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
