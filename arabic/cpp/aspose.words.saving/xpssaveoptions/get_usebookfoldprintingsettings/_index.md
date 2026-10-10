---
title: "طريقة Aspose::Words::Saving::XpsSaveOptions::get_UseBookFoldPrintingSettings"
linktitle: "get_UseBookFoldPrintingSettings"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::XpsSaveOptions::get_UseBookFoldPrintingSettings. يحصل أو يعيّن قيمة منطقية تشير إلى ما إذا كان يجب حفظ المستند باستخدام تخطيط طباعة كتيب، إذا تم تحديده عبر MultiplePages في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.saving/xpssaveoptions/get_usebookfoldprintingsettings/
---
## XpsSaveOptions::get_UseBookFoldPrintingSettings method


يحصل أو يعيّن قيمة منطقية تشير إلى ما إذا كان يجب حفظ المستند باستخدام تخطيط طباعة كتيب، إذا تم تحديده عبر [MultiplePages](../../../aspose.words/pagesetup/get_multiplepages/).

```cpp
bool Aspose::Words::Saving::XpsSaveOptions::get_UseBookFoldPrintingSettings() const
```

## ملاحظات


إذا تم تحديد هذا الخيار، يتم تجاهل [PageSet](../../fixedpagesaveoptions/get_pageset/) عند الحفظ. يتطابق هذا السلوك مع MS Word. إذا لم يتم تحديد إعدادات طباعة الطية في إعداد الصفحة، فلن يكون لهذا الخيار أي تأثير.

## أمثلة



يعرض كيفية حفظ مستند بتنسيق XPS على شكل طيّ كتاب.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

// أنشئ كائن "XpsSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية تحويل تلك الطريقة للمستند إلى .XPS.
auto xpsOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>(Aspose::Words::SaveFormat::Xps);

// اضبط الخاصية "UseBookFoldPrintingSettings" إلى "true" لترتيب المحتويات
// في XPS الناتج بطريقة تساعدنا على استخدامها لإنشاء كتيّب.
// قم بتعيين الخاصية "UseBookFoldPrintingSettings" إلى "false" لعرض XPS بشكل طبيعي.
xpsOptions->set_UseBookFoldPrintingSettings(renderTextAsBookFold);

// إذا كنا نقوم بعرض المستند ككتيب، يجب علينا ضبط "MultiplePages"
// خصائص كائنات إعداد الصفحة لجميع الأقسام إلى "MultiplePagesType.BookFoldPrinting".
if (renderTextAsBookFold)
{
    for (auto&& s : System::IterateOver<Aspose::Words::Section>(doc->get_Sections()))
    {
        s->get_PageSetup()->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::BookFoldPrinting);
    }
}

// بمجرد طباعة هذا المستند، يمكننا تحويله إلى كتيّب عن طريق رص الصفحات.
// للخروج من الطابعة وطيّها في المنتصف.
doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.BookFold.xps", xpsOptions);
```

## انظر أيضًا

* Class [XpsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
