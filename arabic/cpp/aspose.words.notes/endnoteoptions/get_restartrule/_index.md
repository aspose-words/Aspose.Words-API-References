---
title: "طريقة Aspose::Words::Notes::EndnoteOptions::get_RestartRule"
linktitle: "get_RestartRule"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Notes::EndnoteOptions::get_RestartRule. تحدد متى يتم إعادة تشغيل الترقيم التلقائي في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.notes/endnoteoptions/get_restartrule/
---
## EndnoteOptions::get_RestartRule method


يحدد متى يتم إعادة تشغيل الترقيم التلقائي.

```cpp
Aspose::Words::Notes::FootnoteNumberingRule Aspose::Words::Notes::EndnoteOptions::get_RestartRule() override
```

## ملاحظات


ليس كل القيم قابلة للتطبيق على الحواشي النهائية. لتحديد القيم القابلة للتطبيق راجع [FootnoteNumberingRule](../../footnotenumberingrule/).

## أمثلة



يظهر كيفية إعادة تشغيل ترقيم footnote/endnote في أماكن معينة داخل المستند.
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
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 3.");
builder->Write(u"Text 4. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 4.");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 2.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 3.");
builder->Write(u"Text 4. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 4.");

// بشكل افتراضي، رمز المرجع لكل حاشية وحاشية ختامية هو فهرسها
// بين جميع حواشي/حواشي المستند. كل مستند يحتفظ بعدّات منفصلة
// لـ footnotes و endnotes ولا يعيد تشغيل هذه العدادات في أي نقطة.
ASSERT_EQ(doc->get_FootnoteOptions()->get_RestartRule(), Aspose::Words::Notes::FootnoteNumberingRule::Default);
ASSERT_EQ(Aspose::Words::Notes::FootnoteNumberingRule::Default, Aspose::Words::Notes::FootnoteNumberingRule::Continuous);

// يمكننا استخدام الخاصية "RestartRule" لجعل المستند يعيد التشغيل
// عدد footnote/endnote عند صفحة جديدة أو قسم.
doc->get_FootnoteOptions()->set_RestartRule(Aspose::Words::Notes::FootnoteNumberingRule::RestartPage);
doc->get_EndnoteOptions()->set_RestartRule(Aspose::Words::Notes::FootnoteNumberingRule::RestartSection);

doc->Save(get_ArtifactsDir() + u"InlineStory.NumberingRule.docx");
```

## انظر أيضًا

* Enum [FootnoteNumberingRule](../../footnotenumberingrule/)
* Class [EndnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
