---
title: "فئة Aspose::Words::FileFormatInfo"
linktitle: "FileFormatInfo"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::FileFormatInfo. تحتوي على البيانات التي تُرجعها طرق اكتشاف تنسيق المستند في FileFormatUtil. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 27000
url: /ar/cpp/aspose.words/fileformatinfo/
---
## FileFormatInfo class


تحتوي على البيانات التي تُرجعها طرق اكتشاف المستند في [FileFormatUtil](../fileformatutil/). لمعرفة المزيد، زر مقالة الوثائق [Detect File Format and Check Format Compatibility](https://docs.aspose.com/words/cpp/detect-file-format-and-check-format-compatibility/).

```cpp
class FileFormatInfo : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_Encoding](./get_encoding/)() const | يحصل على الترميز المكتشف إذا كان مناسبًا لتنسيق المستند الحالي. في الوقت الحالي يكتشف الترميز فقط للمستندات HTML. |
| [get_HasDigitalSignature](./get_hasdigitalsignature/)() const | يرجع **true** إذا كان هذا المستند يحتوي على توقيع رقمي. هذه الخاصية تُعلم فقط بوجود توقيع رقمي على المستند، لكنها لا تحدد ما إذا كان التوقيع صالحًا أم لا. |
| [get_HasMacros](./get_hasmacros/)() const | يرجع **true** إذا كان هذا المستند يحتوي على ماكرو VBA. |
| [get_IsEncrypted](./get_isencrypted/)() const | يرجع **true** إذا كان المستند مشفرًا ويتطلب كلمة مرور للفتح. |
| [get_LoadFormat](./get_loadformat/)() const | يحصل على تنسيق المستند المكتشف. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## ملاحظات


لا تقوم بإنشاء مثيلات لهذه الفئة مباشرة. تُرجع كائنات هذه الفئة بواسطة طرق [DetectFileFormat()](../).

## أمثلة



يوضح كيفية استخدام فئة [FileFormatUtil](../fileformatutil/) لاكتشاف تنسيق المستند والتشفير.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// قم بتهيئة كائن SaveOptions لتشفير المستند
// مع كلمة مرور عند حفظه، ثم احفظ المستند.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>(Aspose::Words::SaveFormat::Odt);
saveOptions->set_Password(u"MyPassword");

doc->Save(get_ArtifactsDir() + u"File.DetectDocumentEncryption.odt", saveOptions);

// تحقق من نوع ملف مستندنا وحالة تشفيره.
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"File.DetectDocumentEncryption.odt");

ASSERT_EQ(u".odt", Aspose::Words::FileFormatUtil::LoadFormatToExtension(info->get_LoadFormat()));
ASSERT_TRUE(info->get_IsEncrypted());
```


يوضح كيفية استخدام فئة [FileFormatUtil](../fileformatutil/) لاكتشاف تنسيق المستند ووجود التوقيعات الرقمية.
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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
