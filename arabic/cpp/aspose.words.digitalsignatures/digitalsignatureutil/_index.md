---
title: "Aspose::Words::DigitalSignatures::DigitalSignatureUtil فئة"
linktitle: "DigitalSignatureUtil"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::DigitalSignatures::DigitalSignatureUtil فئة. يوفر طرقًا لتوقيع المستند. لمعرفة المزيد، قم بزيارة مقالة الوثائق في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.digitalsignatures/digitalsignatureutil/
---
## DigitalSignatureUtil class


يوفر طرقًا لتوقيع المستند. لمعرفة المزيد، زر مقالة الوثائق [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/).

```cpp
class DigitalSignatureUtil
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [DigitalSignatureUtil](./digitalsignatureutil/)() |  |
| static [LoadSignatures](./loadsignatures/)(const System::String\&) | يقوم بتحميل التوقيعات الرقمية من المستند. |
| static [LoadSignatures](./loadsignatures/)(const System::SharedPtr\<System::IO::Stream\>\&) | يقوم بتحميل التوقيعات الرقمية من المستند باستخدام التدفق. |
| static [LoadSignatures](./loadsignatures/)(std::basic_istream\<CharType, Traits\>\&) |  |
| static [RemoveAllSignatures](./removeallsignatures/)(const System::String\&, const System::String\&) | يزيل جميع التوقيعات الرقمية من ملف المصدر ويكتب ملفًا غير موقع إلى ملف الوجهة. الصيغ التالية متوافقة مع إزالة التوقيع الرقمي: [Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/). |
| static [RemoveAllSignatures](./removeallsignatures/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&) | يزيل جميع التوقيعات الرقمية من المستند في تدفق المصدر ويكتب المستند غير الموقع إلى تدفق الوجهة. **سيتم كتابة الإخراج في بداية التدفق وسيتم تحديث حجم التدفق بطول المحتوى.** الصيغ التالية متوافقة مع إزالة التوقيع الرقمي: [Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/). |
| static [RemoveAllSignatures](./removeallsignatures/)(std::basic_istream\<CharType, Traits\>\&, std::basic_ostream\<CharType, Traits\>\&) |  |
| static [Sign](./sign/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | يوقع المستند المصدر باستخدام [CertificateHolder](../certificateholder/) و[SignOptions](../signoptions/) مع توقيع رقمي ويكتب المستند الموقع إلى تدفق الوجهة. الصيغ المدعومة هي: [Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/). **سيتم كتابة الإخراج في بداية التدفق وسيتم تحديث حجم التدفق بطول المحتوى.** |
| static [Sign](./sign/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | يوقع المستند المصدر باستخدام [CertificateHolder](../certificateholder/) و[SignOptions](../signoptions/) مع توقيع رقمي ويكتب المستند الموقع إلى ملف الوجهة. الصيغ المدعومة هي: [Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/). |
| static [Sign](./sign/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | يوقع المستند المصدر باستخدام [CertificateHolder](../certificateholder/) مع توقيع رقمي ويكتب المستند الموقع إلى تدفق الوجهة. الصيغ المدعومة هي: [Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/). **سيتم كتابة الإخراج في بداية التدفق وسيتم تحديث حجم التدفق بطول المحتوى.** |
| static [Sign](./sign/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | يوقع المستند المصدر باستخدام [CertificateHolder](../certificateholder/) مع توقيع رقمي ويكتب المستند الموقع إلى ملف الوجهة. الصيغ المدعومة هي: [Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/). |
| static [Sign](./sign/)(std::basic_istream\<CharType, Traits\>\&, std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>, System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>) |  |
| static [Sign](./sign/)(std::basic_istream\<CharType, Traits\>\&, std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>) |  |
## ملاحظات


نظرًا لأن التوقيع الرقمي يعمل مع محتوى الملف بدلاً من نموذج كائن [Document](../../aspose.words/document/) يتم وضع هذه الأساليب في فئة منفصلة.

الصيغ المدعومة هي: [Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/).

## أمثلة



يعرض كيفية تحميل التوقيعات من مستند موقع رقمياً.
```cpp
// هناك طريقتان لتحميل مجموعة التوقيعات الرقمية لمستند موقع باستخدام الفئة DigitalSignatureUtil.
// 1 - تحميل من مستند باستخدام اسم ملف من نظام ملفات محلي:
System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> digitalSignatures = Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(get_MyDir() + u"Digitally signed.docx");

// إذا كانت هذه المجموعة غير فارغة، يمكننا التحقق من أن المستند موقع رقمياً.
ASSERT_EQ(1, digitalSignatures->get_Count());

// 2 - تحميل من مستند باستخدام FileStream:
{
    System::SharedPtr<System::IO::Stream> stream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Digitally signed.docx", System::IO::FileMode::Open);
    digitalSignatures = Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(stream);
    ASSERT_EQ(1, digitalSignatures->get_Count());
}
```


يعرض كيفية إزالة التوقيعات الرقمية من مستند موقع رقمياً.
```cpp
// هناك طريقتان لاستخدام فئة DigitalSignatureUtil لإزالة التوقيعات الرقمية
// من مستند موقع عن طريق حفظ نسخة غير موقعة منه في مكان آخر على نظام الملفات المحلي.
// 1 - تحديد مواقع كل من المستند الموقع والنسخة غير الموقعة باستخدام سلاسل أسماء الملفات:
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures(get_MyDir() + u"Digitally signed.docx", get_ArtifactsDir() + u"DigitalSignatureUtil.LoadAndRemove.FromString.docx");

// 2 - تحديد مواقع كل من المستند الموقع والنسخة غير الموقعة باستخدام تدفقات الملفات:
{
    System::SharedPtr<System::IO::Stream> streamIn = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Digitally signed.docx", System::IO::FileMode::Open);
    {
        System::SharedPtr<System::IO::Stream> streamOut = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"DigitalSignatureUtil.LoadAndRemove.FromStream.docx", System::IO::FileMode::Create);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures(streamIn, streamOut);
    }
}

// تحقق من أن كلا مستندينا الناتجين لا يحتويان على توقيعات رقمية.
ASSERT_EQ(0, Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(get_ArtifactsDir() + u"DigitalSignatureUtil.LoadAndRemove.FromString.docx")->get_Count());
ASSERT_EQ(0, Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(get_ArtifactsDir() + u"DigitalSignatureUtil.LoadAndRemove.FromStream.docx")->get_Count());
```

## انظر أيضًا

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
