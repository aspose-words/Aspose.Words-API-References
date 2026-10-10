---
title: "طريقة Aspose::Words::PageSetup::get_HeadingLevelForChapter"
linktitle: "get_HeadingLevelForChapter"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::PageSetup::get_HeadingLevelForChapter. يسترجع أو يعيّن نمط مستوى العنوان الذي يُطبق على عناوين الفصول في المستند في C++."
type: docs
weight: 20000
url: /ar/cpp/aspose.words/pagesetup/get_headinglevelforchapter/
---
## PageSetup::get_HeadingLevelForChapter method


يحصل أو يعيّن نمط مستوى العنوان المطبق على عناوين الفصول في المستند.

```cpp
int32_t Aspose::Words::PageSetup::get_HeadingLevelForChapter()
```

## ملاحظات


يمكن أن يكون رقماً من 0 إلى 9. 0 يعني عدم وجود رقم فصل إذا تم تطبيقه على رقم الصفحة.

قبل أن تتمكن من إنشاء أرقام صفحات تشمل أرقام الفصول، يجب أن تكون عناوين المستند مُطبقةً بتنسيق مخطط مرقّم.

## أمثلة



يُظهر كيفية العمل مع فصول الصفحات.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_FirstSection()->get_PageSetup();

pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);
pageSetup->set_ChapterPageSeparator(Aspose::Words::ChapterPageSeparator::Colon);
pageSetup->set_HeadingLevelForChapter(1);
```

## انظر أيضًا

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
