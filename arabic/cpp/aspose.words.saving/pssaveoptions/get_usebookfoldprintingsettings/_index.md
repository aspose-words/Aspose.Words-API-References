---
title: "Aspose::Words::Saving::PsSaveOptions::get_UseBookFoldPrintingSettings طريقة"
linktitle: "get_UseBookFoldPrintingSettings"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::PsSaveOptions::get_UseBookFoldPrintingSettings طريقة. يحصل أو يضبط قيمة منطقية تشير إلى ما إذا كان يجب حفظ المستند باستخدام تخطيط طباعة كتيب، إذا تم تحديده عبر MultiplePages في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.saving/pssaveoptions/get_usebookfoldprintingsettings/
---
## PsSaveOptions::get_UseBookFoldPrintingSettings method


يحصل أو يعيّن قيمة منطقية تشير إلى ما إذا كان يجب حفظ المستند باستخدام تخطيط طباعة كتيب، إذا تم تحديده عبر [MultiplePages](../../../aspose.words/pagesetup/get_multiplepages/).

```cpp
bool Aspose::Words::Saving::PsSaveOptions::get_UseBookFoldPrintingSettings() const
```

## ملاحظات


إذا تم تحديد هذا الخيار، يتم تجاهل [PageSet](../../fixedpagesaveoptions/get_pageset/) عند الحفظ. يتطابق هذا السلوك مع MS Word. إذا لم يتم تحديد إعدادات طباعة الطية في إعداد الصفحة، فلن يكون لهذا الخيار أي تأثير.

## أمثلة



يظهر كيفية حفظ مستند إلى تنسيق Postscript على شكل طية كتاب.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

// أنشئ كائن "PsSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل طريقة تحويل تلك الطريقة للمستند إلى PostScript.
// اضبط الخاصية "UseBookFoldPrintingSettings" إلى "true" لترتيب المحتويات
// في مستند Postscript الناتج بطريقة تساعدنا على إنشاء كتيب منه.
// اضبط الخاصية "UseBookFoldPrintingSettings" إلى "false" لحفظ المستند بشكل عادي.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::PsSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Ps);
saveOptions->set_UseBookFoldPrintingSettings(renderTextAsBookFold);

// إذا كنا نقوم بعرض المستند ككتيب، يجب علينا ضبط "MultiplePages"
// خصائص كائنات إعداد الصفحة لجميع الأقسام إلى "MultiplePagesType.BookFoldPrinting".
for (auto&& s : System::IterateOver<Aspose::Words::Section>(doc->get_Sections()))
{
    s->get_PageSetup()->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::BookFoldPrinting);
}

// بمجرد طباعة هذا المستند على الوجهين من الصفحات، يمكننا طي جميع الصفحات من الوسط مرة واحدة،
// وستتطابق المحتويات بطريقة تُنشئ كتيّبًا.
doc->Save(get_ArtifactsDir() + u"PsSaveOptions.UseBookFoldPrintingSettings.ps", saveOptions);
```

## انظر أيضًا

* Class [PsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
