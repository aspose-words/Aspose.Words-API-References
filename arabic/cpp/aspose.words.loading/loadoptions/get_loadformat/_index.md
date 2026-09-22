---
title: "Aspose::Words::Loading::LoadOptions::get_LoadFormat method"
linktitle: "get_LoadFormat"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Loading::LoadOptions::get_LoadFormat method. يحدد تنسيق المستند الذي سيتم تحميله. القيمة الافتراضية هي Auto في C++."
type: docs
weight: 10000
url: /ar/cpp/aspose.words.loading/loadoptions/get_loadformat/
---
## LoadOptions::get_LoadFormat method


يحدد تنسيق المستند الذي سيتم تحميله. القيمة الافتراضية هي [Auto](../../../aspose.words/loadformat/).

```cpp
Aspose::Words::LoadFormat Aspose::Words::Loading::LoadOptions::get_LoadFormat() const
```

## ملاحظات


يوصى بتحديد قيمة [Auto](../../../aspose.words/loadformat/) والسماح لـ Aspose.Words باكتشاف تنسيق الملف تلقائيًا. إذا كنت تعرف تنسيق المستند الذي ستقوم بتحميله، يمكنك تحديد التنسيق صراحةً وهذا سيقلل قليلاً من وقت التحميل بسبب العبء المرتبط باكتشاف التنسيق تلقائيًا. إذا قمت بتحديد تنسيق تحميل صريح واتضح أنه غير صحيح، سيتم استدعاء الاكتشاف التلقائي وستُجرى محاولة ثانية لتحميل الملف.

## أمثلة



يعرض كيفية تحديد عنوان URI أساسي عند فتح مستند html.
```cpp
// افترض أننا نريد تحميل مستند .html يحتوي على صورة مرتبطة بعنوان URI نسبي
// في حين أن الصورة موجودة في موقع مختلف. في هذه الحالة، سنحتاج إلى تحويل عنوان URI النسبي إلى عنوان مطلق.
// يمكننا توفير عنوان URI أساسي باستخدام كائن HtmlLoadOptions.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>(Aspose::Words::LoadFormat::Html, u"", get_ImageDir());

ASSERT_EQ(Aspose::Words::LoadFormat::Html, loadOptions->get_LoadFormat());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing image.html", loadOptions);

// بينما كانت الصورة مكسورة في ملف .html المدخل، ساعدنا عنوان URI الأساسي المخصص في إصلاح الرابط.
auto imageShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));
ASSERT_TRUE(imageShape->get_IsImage());

// سيعرض مستند الإخراج هذه الصورة التي كانت مفقودة.
doc->Save(get_ArtifactsDir() + u"HtmlLoadOptions.BaseUri.docx");
```

## انظر أيضًا

* Enum [LoadFormat](../../../aspose.words/loadformat/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
