---
title: "طريقة Aspose::Words::Notes::EndnoteOptions::get_Position"
linktitle: "get_Position"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Notes::EndnoteOptions::get_Position. تحدد موضع الحواشي النهائية في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.notes/endnoteoptions/get_position/
---
## EndnoteOptions::get_Position method


يحدد موضع الحواشي السفلية.

```cpp
Aspose::Words::Notes::EndnotePosition Aspose::Words::Notes::EndnoteOptions::get_Position()
```


## أمثلة



يظهر كيفية اختيار مكان مختلف حيث يجمع المستند ويعرض حواشيه السفلية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// الحاشية السفلية هي طريقة لإرفاق مرجع أو تعليق جانبي بالنص
// الذي لا يتداخل مع تدفق نص الجسم الرئيسي.
// إدراج حاشية سفلية يضيف رمز إشارة صغير مرتفع.
// في نص الجسم الرئيسي حيث نقوم بإدراج الحاشية السفلية.
// كل حاشية سفلية تنشئ أيضًا إدخالًا في نهاية المستند، يتكون من رمز
// يتطابق مع رمز الإشارة في نص الجسم الرئيسي.
// نص الإشارة الذي نمرره إلى طريقة "InsertEndnote" الخاصة بمنشئ المستند.
builder->Write(u"Hello world!");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote contents.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"This is the second section.");

// يمكننا استخدام الخاصية "Position" لتحديد المكان الذي سيضع فيه المستند جميع الحواشي السفلية.
// إذا قمنا بتعيين قيمة الخاصية "Position" إلى "EndnotePosition.EndOfDocument",
// ستظهر كل حاشية سفلية في مجموعة في نهاية المستند. هذه هي القيمة الافتراضية.
// إذا قمنا بتعيين قيمة الخاصية "Position" إلى "EndnotePosition.EndOfSection",
// ستظهر كل حاشية سفلية في مجموعة في نهاية القسم الذي يحتوي نصه على علامة إشارة الحاشية السفلية.
doc->get_EndnoteOptions()->set_Position(endnotePosition);

doc->Save(get_ArtifactsDir() + u"InlineStory.PositionEndnote.docx");
```

## انظر أيضًا

* Enum [EndnotePosition](../../endnoteposition/)
* Class [EndnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
