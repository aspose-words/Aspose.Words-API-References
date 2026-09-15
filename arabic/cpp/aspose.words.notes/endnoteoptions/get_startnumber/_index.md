---
title: "طريقة Aspose::Words::Notes::EndnoteOptions::get_StartNumber"
linktitle: "get_StartNumber"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Notes::EndnoteOptions::get_StartNumber. تحدد الرقم أو الحرف الابتدائي لأول حواشي نهائية مرقمة تلقائيًا في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.notes/endnoteoptions/get_startnumber/
---
## EndnoteOptions::get_StartNumber method


يحدد الرقم أو الحرف الابتدائي للحواشي السفلية المرقمة تلقائيًا الأولى.

```cpp
int32_t Aspose::Words::Notes::EndnoteOptions::get_StartNumber() override
```

## ملاحظات


هذه الخاصية لها تأثير فقط عندما يتم ضبط [RestartRule](../get_restartrule/) إلى [Continuous](../../footnotenumberingrule/).

## أمثلة



يظهر كيفية تعيين رقم يبدأ عنده المستند عدّ footnote/endnote.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// الحواشي والحواشي الختامية هي طريقة لإرفاق مرجع أو تعليق جانبي بالنص
// الذي لا يتداخل مع تدفق نص الجسم الرئيسي.
// إدراج حاشية/حاشية ختامية يضيف رمز مرجع صغير مرتفع
// في نص الجسم الرئيسي حيث نقوم بإدراج الحاشية/الحاشية الختامية.
// كل footnote/endnote ينشئ أيضًا مدخلاً يتكون من رمز
// يتطابق مع رمز الإشارة في نص الجسم الرئيسي.
// نص الإشارة الذي نمرره إلى طريقة "InsertEndnote" الخاصة بمنشئ المستند.
// مدخلات الحواشي، بشكل افتراضي، تظهر في أسفل كل صفحة تحتوي على
// رموز مرجعها، وتظهر الحواشي الختامية في نهاية المستند.
builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 3.");

builder->InsertParagraph();

builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 3.");

// بشكل افتراضي، رمز المرجع لكل حاشية وحاشية ختامية هو فهرسها
// بين جميع حواشي/حواشي المستند. كل مستند يحتفظ بعدّات منفصلة
// لـ footnotes و لـ endnotes، حيث يبدأ كل منهما من 1.
ASSERT_EQ(1, doc->get_FootnoteOptions()->get_StartNumber());
ASSERT_EQ(1, doc->get_EndnoteOptions()->get_StartNumber());

// يمكننا استخدام الخاصية "StartNumber" لجعل المستند يـ
// يبدأ عدّ footnote أو endnote برقم مختلف.
doc->get_EndnoteOptions()->set_NumberStyle(Aspose::Words::NumberStyle::Arabic);
doc->get_EndnoteOptions()->set_StartNumber(50);

doc->Save(get_ArtifactsDir() + u"InlineStory.StartNumber.docx");
```

## انظر أيضًا

* Class [EndnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
