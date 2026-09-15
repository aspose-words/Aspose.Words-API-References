---
title: "طريقة Aspose::Words::Saving::HtmlSaveOptions::get_NavigationMapLevel"
linktitle: "get_NavigationMapLevel"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::HtmlSaveOptions::get_NavigationMapLevel. تحدد الحد الأقصى لمستوى العناوين التي تُملأ في خريطة التنقل عند التصدير إلى صيغ EPUB أو MOBI أو AZW3. القيمة الافتراضية هي %3 في C++."
type: docs
weight: 40500
url: /ar/cpp/aspose.words.saving/htmlsaveoptions/get_navigationmaplevel/
---
## HtmlSaveOptions::get_NavigationMapLevel method


يحدد الحد الأقصى لمستوى العناوين التي تُملأ في خريطة التنقل عند التصدير إلى صيغ EPUB أو MOBI أو AZW3. القيمة الافتراضية هي **%3**.

```cpp
int32_t Aspose::Words::Saving::HtmlSaveOptions::get_NavigationMapLevel() const
```

## ملاحظات


تسمح خريطة التنقل لعوامل المستخدم بتوفير طريقة سهلة للتنقل عبر بنية المستند. عادةً ما تتطابق نقاط التنقل مع العناوين في المستند. لملء العناوين حتى المستوى **N**، قم بتعيين هذه القيمة إلى [NavigationMapLevel](./).

بشكل افتراضي، يتم ملء ثلاثة مستويات من العناوين: فقرات الأنماط **Heading 1** و **Heading 2** و **Heading 3**. يمكنك ضبط هذه الخاصية على قيمة من 1 إلى 9 لطلب المستوى الأقصى المقابل. ضبطها على الصفر سيقلص خريطة التنقل إلى جذر المستند فقط أو جذور أجزاء المستند.

## أمثلة



يوضح كيفية إنشاء جدول محتويات لمستندات Azw3.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Azw3);
options->set_NavigationMapLevel(2);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.CreateAZW3Toc.azw3", options);
```


يوضح كيفية إنشاء جدول محتويات لمستندات Mobi.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Mobi);
options->set_NavigationMapLevel(5);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.CreateMobiToc.mobi", options);
```

## انظر أيضًا

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
