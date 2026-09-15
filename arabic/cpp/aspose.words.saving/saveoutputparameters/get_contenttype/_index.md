---
title: "طريقة Aspose::Words::Saving::SaveOutputParameters::get_ContentType"
linktitle: "get_ContentType"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::SaveOutputParameters::get_ContentType. تُرجع سلسلة Content-Type (نوع وسائط الإنترنت) التي تحدد نوع المستند المحفوظ في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.saving/saveoutputparameters/get_contenttype/
---
## SaveOutputParameters::get_ContentType method


يعيد سلسلة Content-Type (نوع وسائط الإنترنت) التي تحدد نوع المستند المحفوظ.

```cpp
System::String Aspose::Words::Saving::SaveOutputParameters::get_ContentType() const
```


## أمثلة



يوضح كيفية الوصول إلى معلمات الإخراج لعملية حفظ المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// بعد حفظ المستند، يمكننا الوصول إلى نوع وسائط الإنترنت (نوع MIME) للمستند الناتج الذي تم إنشاؤه حديثًا.
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> parameters = doc->Save(get_ArtifactsDir() + u"Document.SaveOutputParameters.doc");

ASSERT_EQ(u"application/msword", parameters->get_ContentType());

// تتغير هذه الخاصية اعتمادًا على صيغة الحفظ.
parameters = doc->Save(get_ArtifactsDir() + u"Document.SaveOutputParameters.pdf");

ASSERT_EQ(u"application/pdf", parameters->get_ContentType());
```

## انظر أيضًا

* Class [SaveOutputParameters](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
