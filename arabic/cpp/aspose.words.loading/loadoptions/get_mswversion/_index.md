---
title: "Aspose::Words::Loading::LoadOptions::get_MswVersion method"
linktitle: "get_MswVersion"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Loading::LoadOptions::get_MswVersion method. يسمح بتحديد أن عملية تحميل المستند يجب أن تتطابق مع إصدار معين من MS Word. القيمة الافتراضية هي Word2019 في C++."
type: docs
weight: 11000
url: /ar/cpp/aspose.words.loading/loadoptions/get_mswversion/
---
## LoadOptions::get_MswVersion method


يسمح بتحديد أن عملية تحميل المستند يجب أن تتطابق مع إصدار معين من MS Word. القيمة الافتراضية هي [Word2019](../../../aspose.words.settings/mswordversion/)

```cpp
Aspose::Words::Settings::MsWordVersion Aspose::Words::Loading::LoadOptions::get_MswVersion() const
```


## أمثلة



يوضح كيفية محاكاة إجراء التحميل لإصدار معين من Microsoft Word أثناء تحميل المستند.
```cpp
// بشكل افتراضي، يقوم Aspose.Words بتحميل المستندات وفقًا لمواصفات Microsoft Word 2019.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();

ASSERT_EQ(Aspose::Words::Settings::MsWordVersion::Word2019, loadOptions->get_MswVersion());

// هذا المستند يفتقد نمط تنسيق الفقرة الافتراضي.
// سيتم إعادة إنشاء هذا النمط الافتراضي عندما نقوم بتحميل المستند إما باستخدام Microsoft Word أو Aspose.Words.
loadOptions->set_MswVersion(Aspose::Words::Settings::MsWordVersion::Word2007);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx", loadOptions);

// سيتضمن تباعد الأسطر للنمط هذه القيمة عند تحميله وفقًا لمواصفات Microsoft Word 2007.
ASSERT_NEAR(12.95, doc->get_Styles()->get_DefaultParagraphFormat()->get_LineSpacing(), 0.01);
```

## انظر أيضًا

* Enum [MsWordVersion](../../../aspose.words.settings/mswordversion/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
