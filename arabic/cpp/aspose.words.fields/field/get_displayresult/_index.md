---
title: "طريقة Aspose::Words::Fields::Field::get_DisplayResult"
linktitle: "get_DisplayResult"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::Field::get_DisplayResult. يحصل على النص الذي يمثل نتيجة الحقل المعروضة في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.fields/field/get_displayresult/
---
## Field::get_DisplayResult method


يحصل على النص الذي يمثل نتيجة الحقل المعروضة.

```cpp
System::String Aspose::Words::Fields::Field::get_DisplayResult()
```


## أمثلة



يعرض كيفية الحصول على النص الحقيقي الذي يعرضه الحقل في المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"This document was written by ");
auto fieldAuthor = System::ExplicitCast<Aspose::Words::Fields::FieldAuthor>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true));
fieldAuthor->set_AuthorName(u"John Doe");

// يمكننا استخدام خاصية DisplayResult للتحقق من النص الدقيق
// الذي سيعرضه الحقل في موضعه داخل المستند.
ASSERT_EQ(System::String::Empty, fieldAuthor->get_DisplayResult());

// الحقول لا تحتفظ بقيم النتائج الدقيقة في الوقت الحقيقي.
// للتأكد من أن حقولنا تعرض نتائج دقيقة في أي وقت،
// مثلًا قبل عملية الحفظ مباشرةً، نحتاج إلى تحديثها يدويًا.
fieldAuthor->Update();

ASSERT_EQ(u"John Doe", fieldAuthor->get_DisplayResult());

doc->Save(get_ArtifactsDir() + u"Field.DisplayResult.docx");
```

## انظر أيضًا

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
