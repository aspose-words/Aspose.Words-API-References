---
title: "طريقة Aspose::Words::Loading::LoadOptions::get_Encoding"
linktitle: "get_Encoding"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Loading::LoadOptions::get_Encoding. يحصل على أو يحدد الترميز الذي سيُستخدم لتحميل مستند HTML أو TXT أو CHM إذا لم يُحدد الترميز داخل المستند. يمكن أن تكون null. القيمة الافتراضية هي null في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.loading/loadoptions/get_encoding/
---
## LoadOptions::get_Encoding method


يحصل أو يعيّن الترميز الذي سيُستخدم لتحميل مستند HTML أو TXT أو CHM إذا لم يتم تحديد الترميز داخل المستند. يمكن أن يكون **null**. القيمة الافتراضية هي **null**.

```cpp
System::SharedPtr<System::Text::Encoding> Aspose::Words::Loading::LoadOptions::get_Encoding() const
```

## ملاحظات


هذه الخاصية تُستخدم فقط عند تحميل مستندات HTML أو TXT أو CHM.

إذا لم يُحدد الترميز داخل المستند وكانت هذه الخاصية **null**، فستحاول النظام اكتشاف الترميز تلقائيًا.

## أمثلة



يوضح كيفية تعيين الترميز لفتح مستند.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_Encoding(System::Text::Encoding::get_ASCII());

// حمّل المستند مع تمرير كائن LoadOptions، ثم تحقق من محتويات المستند.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"English text.txt", loadOptions);

ASSERT_TRUE(doc->ToString(Aspose::Words::SaveFormat::Text).Contains(u"This is a sample text in English."));
```

## انظر أيضًا

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
