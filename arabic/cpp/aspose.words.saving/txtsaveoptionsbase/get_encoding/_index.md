---
title: "طريقة Aspose::Words::Saving::TxtSaveOptionsBase::get_Encoding"
linktitle: "get_Encoding"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::TxtSaveOptionsBase::get_Encoding. يحدد الترميز الذي يُستخدم عند التصدير بصيغ النص. القيمة الافتراضية هي Encoding.UTF8 في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.saving/txtsaveoptionsbase/get_encoding/
---
## TxtSaveOptionsBase::get_Encoding method


يحدد الترميز المستخدم عند التصدير إلى تنسيقات نصية. القيمة الافتراضية هي **Encoding.UTF8**.

```cpp
System::SharedPtr<System::Text::Encoding> Aspose::Words::Saving::TxtSaveOptionsBase::get_Encoding() const
```


## أمثلة



يوضح كيفية تعيين الترميز لمستند إخراج .txt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أضف بعض النصوص التي تحتوي على أحرف خارج مجموعة أحرف ASCII.
builder->Write(u"À È Ì Ò Ù.");

// إنشاء كائن "TxtSaveOptions"، والذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل طريقة حفظ المستند كنص عادي.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// تحقق من أن الخاصية "Encoding" تحتوي على الترميز المناسب لمحتويات مستندنا.
ASPOSE_ASSERT_EQ(System::Text::Encoding::get_UTF8(), txtSaveOptions->get_Encoding());

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.Encoding.UTF8.txt", txtSaveOptions);

System::String docText = System::Text::Encoding::get_UTF8()->GetString(System::IO::File::ReadAllBytes(get_ArtifactsDir() + u"TxtSaveOptions.Encoding.UTF8.txt"));

ASSERT_EQ(u"\ufeffÀ È Ì Ò Ù.\r\n", docText);

// استخدام ترميز غير مناسب قد يؤدي إلى فقدان محتوى المستند.
txtSaveOptions->set_Encoding(System::Text::Encoding::get_ASCII());
doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.Encoding.ASCII.txt", txtSaveOptions);
docText = System::Text::Encoding::get_ASCII()->GetString(System::IO::File::ReadAllBytes(get_ArtifactsDir() + u"TxtSaveOptions.Encoding.ASCII.txt"));

ASSERT_EQ(u"? ? ? ? ?.\r\n", docText);
```

## انظر أيضًا

* Class [TxtSaveOptionsBase](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
