---
title: "طريقة Aspose::Words::PageSetup::get_ChapterPageSeparator"
linktitle: "get_ChapterPageSeparator"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::PageSetup::get_ChapterPageSeparator. يحصل أو يعيّن حرف الفاصل الذي يظهر بين رقم الفصل ورقم الصفحة في C++."
type: docs
weight: 11000
url: /ar/cpp/aspose.words/pagesetup/get_chapterpageseparator/
---
## PageSetup::get_ChapterPageSeparator method


يحصل أو يعيّن حرف الفاصل الذي يظهر بين رقم الفصل ورقم الصفحة.

```cpp
Aspose::Words::ChapterPageSeparator Aspose::Words::PageSetup::get_ChapterPageSeparator()
```

## ملاحظات


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

* Enum [ChapterPageSeparator](../../chapterpageseparator/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
