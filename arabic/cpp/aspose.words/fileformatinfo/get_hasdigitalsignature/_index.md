---
title: "طريقة Aspose::Words::FileFormatInfo::get_HasDigitalSignature"
linktitle: "get_HasDigitalSignature"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::FileFormatInfo::get_HasDigitalSignature. تُعيد true إذا كان هذا المستند يحتوي على توقيع رقمي. هذه الخاصية تُخبر فقط بوجود توقيع رقمي على المستند، لكنها لا تحدد ما إذا كان التوقيع صالحًا أم لا في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words/fileformatinfo/get_hasdigitalsignature/
---
## FileFormatInfo::get_HasDigitalSignature method


يرجع **true** إذا كان هذا المستند يحتوي على توقيع رقمي. هذه الخاصية تُعلم فقط بوجود توقيع رقمي على المستند، لكنها لا تحدد ما إذا كان التوقيع صالحًا أم لا.

```cpp
bool Aspose::Words::FileFormatInfo::get_HasDigitalSignature() const
```

## ملاحظات


هذه الخاصية موجودة لمساعدتك في فرز المستندات الموقعة رقمياً عن غير الموقعة. إذا استخدمت Aspose.Words لتعديل وحفظ مستند موقّع رقمياً، فسيتم فقدان التوقيع الرقمي. هذا مقصود لأن التوقيع الرقمي موجود لحماية أصالة المستند. باستخدام هذه الخاصية يمكنك اكتشاف المستندات الموقعة رقمياً قبل معالجتها بنفس طريقة المستندات العادية واتخاذ إجراء لتجنب فقدان التوقيع الرقمي، على سبيل المثال إبلاغ المستخدم.

## أمثلة



يظهر كيفية استخدام الفئة [FileFormatUtil](../../fileformatutil/) لاكتشاف تنسيق المستند ووجود التوقيعات الرقمية.
```cpp
// استخدم مثيل FileFormatInfo للتحقق من أن المستند غير موقع رقمياً.
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.docx");

ASSERT_EQ(u".docx", Aspose::Words::FileFormatUtil::LoadFormatToExtension(info->get_LoadFormat()));
ASSERT_FALSE(info->get_HasDigitalSignature());

System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw", nullptr);
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_SignTime(System::DateTime::get_Now());
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(get_MyDir() + u"Document.docx", get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx", certificateHolder, signOptions);

// استخدم FileFormatInstance جديدًا لتأكيد أنه موقع.
info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx");

ASSERT_TRUE(info->get_HasDigitalSignature());

// يمكننا تحميل والوصول إلى توقيعات مستند موقع في مجموعة مثل هذه.
ASSERT_EQ(1, Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx")->get_Count());
```

## انظر أيضًا

* Class [FileFormatInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
