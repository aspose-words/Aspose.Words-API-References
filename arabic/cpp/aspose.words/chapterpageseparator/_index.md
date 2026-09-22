---
title: "Aspose::Words::ChapterPageSeparator enum"
linktitle: "ChapterPageSeparator"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::ChapterPageSeparator enum. يحدد حرف الفاصل الذي يظهر بين رقم الفصل ورقم الصفحة في C++."
type: docs
weight: 84000
url: /ar/cpp/aspose.words/chapterpageseparator/
---
## ChapterPageSeparator enum


يعرف حرف الفاصل الذي يظهر بين رقم الفصل ورقم الصفحة.

```cpp
enum class ChapterPageSeparator
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| شرطة | 0 | نقطتان رأسيتان. |
| نقطة | 1 | نقطة. |
| نقطتان رأسيتان | 2 | نقطتان رأسيتان. |
| شرطة طويلة | 3 | شرطة مميزة. |
| شرطة متوسطة | 4 | شرطة قياسية. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
