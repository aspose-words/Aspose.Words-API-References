---
title: "طريقة Aspose::Words::Notes::EndnoteOptions::get_NumberStyle"
linktitle: "get_NumberStyle"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Notes::EndnoteOptions::get_NumberStyle. تحدد تنسيق الرقم للحواشي النهائية المرقمة تلقائيًا في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.notes/endnoteoptions/get_numberstyle/
---
## EndnoteOptions::get_NumberStyle method


يحدد تنسيق الرقم للهوامش النهائية المرقمة تلقائيًا.

```cpp
Aspose::Words::NumberStyle Aspose::Words::Notes::EndnoteOptions::get_NumberStyle() override
```

## ملاحظات


ليس كل أنماط الأرقام قابلة للتطبيق على هذه الخاصية. للحصول على قائمة بأنماط الأرقام القابلة للتطبيق، راجع مربع حوار إدراج [Footnote](../../footnote/) أو الحاشية السفلية في Microsoft Word. إذا اخترت نمط رقم غير قابل للتطبيق، سيعود Microsoft Word إلى القيمة الافتراضية.

## أمثلة



يعرض كيفية تغيير نمط رقم علامات مرجع الحاشية/الحاشية الختامية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// الحواشي والحواشي الختامية هي طريقة لإرفاق مرجع أو تعليق جانبي بالنص
// الذي لا يتداخل مع تدفق نص الجسم الرئيسي.
// إدراج حاشية/حاشية ختامية يضيف رمز مرجع صغير مرتفع
// في نص الجسم الرئيسي حيث نقوم بإدراج الحاشية/الحاشية الختامية.
// كل حاشية/حاشية ختامية تنشئ أيضًا مدخلاً يتكون من رمز يطابق المرجع
// الرمز في نص الجسم الرئيسي. نص المرجع الذي نمرره إلى طريقة "InsertEndnote" في مُنشئ المستند.
// مدخلات الحواشي، بشكل افتراضي، تظهر في أسفل كل صفحة تحتوي على
// رموز مرجعها، وتظهر الحواشي الختامية في نهاية المستند.
builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 3.", u"Custom footnote reference mark");

builder->InsertParagraph();

builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 3.", u"Custom endnote reference mark");

// بشكل افتراضي، رمز المرجع لكل حاشية وحاشية ختامية هو فهرسها
// بين جميع حواشي/حواشي المستند. كل مستند يحتفظ بعدّات منفصلة
// للحواشي وللحواشي الختامية. بشكل افتراضي، تعرض الحواشي أرقامها باستخدام الأرقام العربية،
// وتعرض الحواشي الختامية أرقامها بالأحرف الرومانية الصغيرة.
ASSERT_EQ(Aspose::Words::NumberStyle::Arabic, doc->get_FootnoteOptions()->get_NumberStyle());
ASSERT_EQ(Aspose::Words::NumberStyle::LowercaseRoman, doc->get_EndnoteOptions()->get_NumberStyle());

// يمكننا استخدام الخاصية "NumberStyle" لتطبيق أنماط ترقيم مخصصة على الحواشي والحواشي الختامية.
// هذا لن يؤثر على الحواشي/الحواشي الختامية ذات علامات مرجع مخصصة.
doc->get_FootnoteOptions()->set_NumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);
doc->get_EndnoteOptions()->set_NumberStyle(Aspose::Words::NumberStyle::UppercaseLetter);

doc->Save(get_ArtifactsDir() + u"InlineStory.RefMarkNumberStyle.docx");
```

## انظر أيضًا

* Enum [NumberStyle](../../../aspose.words/numberstyle/)
* Class [EndnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
