---
title: "تعداد Aspose::Words::Loading::DocumentDirection"
linktitle: "DocumentDirection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "تعداد Aspose::Words::Loading::DocumentDirection. يسمح بتحديد اتجاه تدفق النص في المستند بلغة C++."
type: docs
weight: 13000
url: /ar/cpp/aspose.words.loading/documentdirection/
---
## DocumentDirection enum


يسمح بتحديد اتجاه تدفق النص في المستند.

```cpp
enum class DocumentDirection
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| LeftToRight | 0 | اتجاه من اليسار إلى اليمين. |
| RightToLeft | 1 | اتجاه من اليمين إلى اليسار. |
| تلقائي | 2 | اكتشاف الاتجاه تلقائيًا. |


## أمثلة



يُظهر كيفية اكتشاف اتجاه نص المستند النصي.
```cpp
// إنشاء كائن "TxtLoadOptions"، والذي يمكننا تمريره إلى مُنشئ المستند
// لتعديل طريقة تحميل المستند النصي.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();

// عيّن خاصية "DocumentDirection" إلى "DocumentDirection.Auto" لاكتشاف تلقائيًا
// اتجاه كل فقرة نصية يقوم Aspose.Words بتحميلها من النص العادي.
// ستخزن خاصية "Bidi" لكل فقرة اتجاهها.
loadOptions->set_DocumentDirection(Aspose::Words::Loading::DocumentDirection::Auto);

// اكتشاف النص العبري كمن اليمين إلى اليسار.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Hebrew text.txt", loadOptions);

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Bidi());

// اكتشاف النص الإنجليزي كمن اليمين إلى اليسار.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"English text.txt", loadOptions);

ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Bidi());
```

## انظر أيضًا

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
