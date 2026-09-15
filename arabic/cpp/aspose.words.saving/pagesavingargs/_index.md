---
title: "Aspose::Words::Saving::PageSavingArgs فئة"
linktitle: "PageSavingArgs"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::PageSavingArgs فئة. يوفر بيانات لحدث PageSaving(). لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 19000
url: /ar/cpp/aspose.words.saving/pagesavingargs/
---
## PageSavingArgs class


يوفر بيانات لحدث [PageSaving()](../ipagesavingcallback/pagesaving/). لمعرفة المزيد، زر مقالة الوثائق [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class PageSavingArgs : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_KeepPageStreamOpen](./get_keeppagestreamopen/)() const | يحدد ما إذا كان يجب على Aspose.Words إبقاء الدفق مفتوحًا أو إغلاقه بعد حفظ صفحة المستند. |
| [get_PageFileName](./get_pagefilename/)() const | يحصل على اسم الملف حيث سيتم حفظ صفحة المستند. |
| [get_PageIndex](./get_pageindex/)() const | فهرس الصفحة الحالي. |
| [get_PageStream](./get_pagestream/)() const | يسمح بتحديد الدفق حيث سيتم حفظ صفحة المستند. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PageSavingArgs](./pagesavingargs/)() |  |
| [set_KeepPageStreamOpen](./set_keeppagestreamopen/)(bool) | مُعيّن لـ [Aspose::Words::Saving::PageSavingArgs::get_KeepPageStreamOpen](./get_keeppagestreamopen/). |
| [set_PageFileName](./set_pagefilename/)(const System::String\&) | يحدد اسم الملف حيث سيتم حفظ صفحة المستند. |
| [set_PageStream](./set_pagestream/)(const System::SharedPtr\<System::IO::Stream\>\&) | مُعيّن لـ [Aspose::Words::Saving::PageSavingArgs::get_PageStream](./get_pagestream/). |
| [set_PageStream](./set_pagestream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| static [Type](./type/)() |  |
## انظر أيضًا

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
