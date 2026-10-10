---
title: "طريقة Aspose::Words::Loading::TxtLoadOptions::get_DocumentDirection"
linktitle: "get_DocumentDirection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Loading::TxtLoadOptions::get_DocumentDirection. يحصل أو يضبط اتجاه المستند. القيمة الافتراضية هي LeftToRight في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.loading/txtloadoptions/get_documentdirection/
---
## TxtLoadOptions::get_DocumentDirection method


يحصل أو يضبط اتجاه المستند. القيمة الافتراضية هي [LeftToRight](../../documentdirection/).

```cpp
Aspose::Words::Loading::DocumentDirection Aspose::Words::Loading::TxtLoadOptions::get_DocumentDirection() const
```


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

* Enum [DocumentDirection](../../documentdirection/)
* Class [TxtLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
