---
title: "Aspose::Words::Saving::PsSaveOptions::get_SaveFormat طريقة"
linktitle: "get_SaveFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::PsSaveOptions::get_SaveFormat طريقة. يحدد التنسيق الذي سيتم حفظ المستند به إذا تم استخدام كائن خيارات الحفظ هذا. يمكن أن يكون فقط Ps في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.saving/pssaveoptions/get_saveformat/
---
## PsSaveOptions::get_SaveFormat method


يحدد التنسيق الذي سيتم حفظ المستند به إذا تم استخدام كائن خيارات الحفظ هذا. يمكن أن يكون فقط [Ps](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::PsSaveOptions::get_SaveFormat() override
```


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

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [PsSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
