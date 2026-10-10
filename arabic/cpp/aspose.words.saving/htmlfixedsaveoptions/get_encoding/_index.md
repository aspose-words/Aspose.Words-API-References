---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_Encoding طريقة"
linktitle: "get_Encoding"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_Encoding طريقة. يحدد الترميز الذي سيُستخدم عند التصدير إلى HTML. القيمة الافتراضية هي new UTF8Encoding(true) (UTF-8 مع BOM) في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.saving/htmlfixedsaveoptions/get_encoding/
---
## HtmlFixedSaveOptions::get_Encoding method


يحدد الترميز المستخدم عند التصدير إلى HTML. القيمة الافتراضية هي **new UTF8Encoding(true)** (UTF-8 مع BOM).

```cpp
System::SharedPtr<System::Text::Encoding> Aspose::Words::Saving::HtmlFixedSaveOptions::get_Encoding() const
```


## أمثلة



يوضح كيفية تحديد الترميز الذي سيُستخدم أثناء تصدير المستند إلى HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello World!");

// الترميز الافتراضي هو UTF-8. إذا أردنا تمثيل مستندنا باستخدام ترميز مختلف،
// يمكننا استخدام كائن SaveOptions لتعيين ترميز محدد.
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_Encoding(System::Text::Encoding::get_ASCII());

ASSERT_EQ(u"US-ASCII", htmlFixedSaveOptions->get_Encoding()->get_EncodingName());

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.UseEncoding.html", htmlFixedSaveOptions);
```

## انظر أيضًا

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
