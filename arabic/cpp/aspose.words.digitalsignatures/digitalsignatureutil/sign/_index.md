---
title: "طريقة Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign"
linktitle: "توقيع"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign. يوقع المستند المصدر باستخدام CertificateHolder المقدم مع توقيع رقمي ويكتب المستند الموقع إلى تدفق الوجهة. الصيغ المدعومة هي: Doc, Dot, Docx, Dotx, Docm, Dotm, Odt, Ott. سيتم كتابة الإخراج في بداية التدفق وسيتم تحديث حجم التدفق بطول المحتوى في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.digitalsignatures/digitalsignatureutil/sign/
---
## DigitalSignatureUtil::Sign(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) method


يوقع المستند المصدر باستخدام [CertificateHolder](../../certificateholder/) المقدم مع توقيع رقمي ويكتب المستند الموقع إلى تدفق الوجهة. الصيغ المدعومة هي: [Doc](../../../aspose.words/loadformat/), [Dot](../../../aspose.words/loadformat/), [Docx](../../../aspose.words/loadformat/), [Dotx](../../../aspose.words/loadformat/), [Docm](../../../aspose.words/loadformat/), [Dotm](../../../aspose.words/loadformat/), [Odt](../../../aspose.words/loadformat/), [Ott](../../../aspose.words/loadformat/). **سيتم كتابة الإخراج في بداية التدفق وسيتم تحديث حجم التدفق بطول المحتوى.**

```cpp
static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(const System::SharedPtr<System::IO::Stream> &srcStream, const System::SharedPtr<System::IO::Stream> &dstStream, const System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> &certHolder)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| srcStream | const System::SharedPtr\<System::IO::Stream\>\& | التدفق الذي يحتوي على المستند لتوقيعه. |
| dstStream | const System::SharedPtr\<System::IO::Stream\>\& | التدفق الذي سيُكتب إليه المستند الموقع. |
| certHolder | const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\& | [CertificateHolder](../../certificateholder/) كائن مع شهادة تم استخدامها لتوقيع الملف. يجب أن تحتوي الشهادة في الحامل على مفاتيح خاصة. |

## أمثلة



يوضح كيفية توقيع المستندات باستخدام شهادات X.509.
```cpp
// تحقق من أن المستند غير موقع.
ASSERT_FALSE(Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.docx")->get_HasDigitalSignature());

// إنشاء كائن CertificateHolder من ملف PKCS12، والذي سنستخدمه لتوقيع المستند.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw", nullptr);

// هناك طريقتان لحفظ نسخة موقعة من المستند على نظام الملفات المحلي:
// 1 - تحديد مستند باسم ملف نظام محلي وحفظ نسخة موقعة في موقع يحدده اسم ملف آخر.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_SignTime(System::DateTime::get_Now());
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(get_MyDir() + u"Document.docx", get_ArtifactsDir() + u"Document.DigitalSignature.docx", certificateHolder, signOptions);

ASSERT_TRUE(Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"Document.DigitalSignature.docx")->get_HasDigitalSignature());

// 2 - أخذ مستند من تدفق وحفظ نسخة موقعة إلى تدفق آخر.
{
    auto inDoc = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Document.docx", System::IO::FileMode::Open);
    {
        auto outDoc = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"Document.DigitalSignature.docx", System::IO::FileMode::Create);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inDoc, outDoc, certificateHolder);
    }
}

ASSERT_TRUE(Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"Document.DigitalSignature.docx")->get_HasDigitalSignature());

// يرجى التحقق من أن جميع التوقيعات الرقمية للمستند صالحة والتحقق من تفاصيلها.
auto signedDoc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.DigitalSignature.docx");
System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> digitalSignatureCollection = signedDoc->get_DigitalSignatures();

ASSERT_TRUE(digitalSignatureCollection->get_IsValid());
ASSERT_EQ(1, digitalSignatureCollection->get_Count());
ASSERT_EQ(Aspose::Words::DigitalSignatures::DigitalSignatureType::XmlDsig, digitalSignatureCollection->idx_get(0)->get_SignatureType());
ASSERT_EQ(u"CN=Morzal.Me", signedDoc->get_DigitalSignatures()->idx_get(0)->get_IssuerName());
ASSERT_EQ(u"CN=Morzal.Me", signedDoc->get_DigitalSignatures()->idx_get(0)->get_SubjectName());
```

## انظر أيضًا

* Class [CertificateHolder](../../certificateholder/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::Sign(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) method


يوقع مستند المصدر باستخدام [CertificateHolder](../../certificateholder/) و [SignOptions](../../signoptions/) مع توقيع رقمي ويكتب المستند الموقع إلى تدفق الوجهة. الصيغ المدعومة هي: [Doc](../../../aspose.words/loadformat/), [Dot](../../../aspose.words/loadformat/), [Docx](../../../aspose.words/loadformat/), [Dotx](../../../aspose.words/loadformat/), [Docm](../../../aspose.words/loadformat/), [Dotm](../../../aspose.words/loadformat/), [Odt](../../../aspose.words/loadformat/), [Ott](../../../aspose.words/loadformat/).**سيتم كتابة الإخراج في بداية التدفق وسيتم تحديث حجم التدفق بطول المحتوى.**

```cpp
static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(const System::SharedPtr<System::IO::Stream> &srcStream, const System::SharedPtr<System::IO::Stream> &dstStream, const System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> &certHolder, const System::SharedPtr<Aspose::Words::DigitalSignatures::SignOptions> &signOptions)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| srcStream | const System::SharedPtr\<System::IO::Stream\>\& | التدفق الذي يحتوي على المستند لتوقيعه. |
| dstStream | const System::SharedPtr\<System::IO::Stream\>\& | التدفق الذي سيُكتب إليه المستند الموقع. |
| certHolder | const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\& | [CertificateHolder](../../certificateholder/) كائن مع شهادة تم استخدامها لتوقيع الملف. يجب أن تحتوي الشهادة في الحامل على مفاتيح خاصة. |
| signOptions | const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\& | كائن [SignOptions](../../signoptions/) مع خيارات توقيع متنوعة. |

## أمثلة



يوضح كيفية توقيع المستندات رقمياً.
```cpp
// إنشاء شهادة X.509 من مخزن PKCS#12، والذي يجب أن يحتوي على مفتاح خاص.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

// إنشاء تعليق وتاريخ سيتم تطبيقهما مع توقيعنا الرقمي الجديد.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"My comment");
signOptions->set_SignTime(System::DateTime::get_Now());

// أخذ مستند غير موقع من نظام الملفات المحلي عبر تدفق ملف،
// ثم إنشاء نسخة موقعة منه يتم تحديدها بواسطة اسم ملف تدفق الإخراج.
{
    System::SharedPtr<System::IO::Stream> streamIn = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Document.docx", System::IO::FileMode::Open);
    {
        System::SharedPtr<System::IO::Stream> streamOut = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"DigitalSignatureUtil.SignDocument.docx", System::IO::FileMode::OpenOrCreate);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

## انظر أيضًا

* Class [CertificateHolder](../../certificateholder/)
* Class [SignOptions](../../signoptions/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::Sign(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) method


يوقع مستند المصدر باستخدام [CertificateHolder](../../certificateholder/) مع توقيع رقمي ويكتب المستند الموقع إلى ملف الوجهة. الصيغ المدعومة هي: [Doc](../../../aspose.words/loadformat/), [Dot](../../../aspose.words/loadformat/), [Docx](../../../aspose.words/loadformat/), [Dotx](../../../aspose.words/loadformat/), [Docm](../../../aspose.words/loadformat/), [Dotm](../../../aspose.words/loadformat/), [Odt](../../../aspose.words/loadformat/), [Ott](../../../aspose.words/loadformat/).

```cpp
static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(const System::String &srcFileName, const System::String &dstFileName, const System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> &certHolder)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| srcFileName | const System::String\& | اسم ملف المستند الذي سيتم توقيعه. |
| dstFileName | const System::String\& | اسم ملف المستند الموقع الناتج. |
| certHolder | const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\& | [CertificateHolder](../../certificateholder/) كائن مع شهادة تم استخدامها لتوقيع الملف. يجب أن تحتوي الشهادة في الحامل على مفاتيح خاصة. |

## أمثلة



يوضح كيفية توقيع المستندات باستخدام شهادات X.509.
```cpp
// تحقق من أن المستند غير موقع.
ASSERT_FALSE(Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.docx")->get_HasDigitalSignature());

// إنشاء كائن CertificateHolder من ملف PKCS12، والذي سنستخدمه لتوقيع المستند.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw", nullptr);

// هناك طريقتان لحفظ نسخة موقعة من المستند على نظام الملفات المحلي:
// 1 - تحديد مستند باسم ملف نظام محلي وحفظ نسخة موقعة في موقع يحدده اسم ملف آخر.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_SignTime(System::DateTime::get_Now());
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(get_MyDir() + u"Document.docx", get_ArtifactsDir() + u"Document.DigitalSignature.docx", certificateHolder, signOptions);

ASSERT_TRUE(Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"Document.DigitalSignature.docx")->get_HasDigitalSignature());

// 2 - أخذ مستند من تدفق وحفظ نسخة موقعة إلى تدفق آخر.
{
    auto inDoc = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Document.docx", System::IO::FileMode::Open);
    {
        auto outDoc = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"Document.DigitalSignature.docx", System::IO::FileMode::Create);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inDoc, outDoc, certificateHolder);
    }
}

ASSERT_TRUE(Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"Document.DigitalSignature.docx")->get_HasDigitalSignature());

// يرجى التحقق من أن جميع التوقيعات الرقمية للمستند صالحة والتحقق من تفاصيلها.
auto signedDoc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.DigitalSignature.docx");
System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> digitalSignatureCollection = signedDoc->get_DigitalSignatures();

ASSERT_TRUE(digitalSignatureCollection->get_IsValid());
ASSERT_EQ(1, digitalSignatureCollection->get_Count());
ASSERT_EQ(Aspose::Words::DigitalSignatures::DigitalSignatureType::XmlDsig, digitalSignatureCollection->idx_get(0)->get_SignatureType());
ASSERT_EQ(u"CN=Morzal.Me", signedDoc->get_DigitalSignatures()->idx_get(0)->get_IssuerName());
ASSERT_EQ(u"CN=Morzal.Me", signedDoc->get_DigitalSignatures()->idx_get(0)->get_SubjectName());
```

## انظر أيضًا

* Class [CertificateHolder](../../certificateholder/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::Sign(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) method


يوقع مستند المصدر باستخدام [CertificateHolder](../../certificateholder/) و [SignOptions](../../signoptions/) مع توقيع رقمي ويكتب المستند الموقع إلى ملف الوجهة. الصيغ المدعومة هي: [Doc](../../../aspose.words/loadformat/), [Dot](../../../aspose.words/loadformat/), [Docx](../../../aspose.words/loadformat/), [Dotx](../../../aspose.words/loadformat/), [Docm](../../../aspose.words/loadformat/), [Dotm](../../../aspose.words/loadformat/), [Odt](../../../aspose.words/loadformat/), [Ott](../../../aspose.words/loadformat/).

```cpp
static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(const System::String &srcFileName, const System::String &dstFileName, const System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> &certHolder, const System::SharedPtr<Aspose::Words::DigitalSignatures::SignOptions> &signOptions)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| srcFileName | const System::String\& | اسم ملف المستند الذي سيتم توقيعه. |
| dstFileName | const System::String\& | اسم ملف المستند الموقع الناتج. |
| certHolder | const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\& | [CertificateHolder](../../certificateholder/) كائن مع شهادة تم استخدامها لتوقيع الملف. يجب أن تحتوي الشهادة في الحامل على مفاتيح خاصة. |
| signOptions | const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\& | كائن [SignOptions](../../signoptions/) مع خيارات توقيع متنوعة. |

## أمثلة



يوضح كيفية توقيع مستند مع خيارات توقيع إضافية.
```cpp
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_WindowsVersion(u"10.0");
signOptions->set_ApplicationVersion(u"16.0.19127");
signOptions->set_OfficeVersion(u"16.0.19127/27");
signOptions->set_HorizontalResolution(1024);
signOptions->set_VerticalResolution(768);
signOptions->set_ColorDepth(24);

System::ArrayPtr<uint8_t> certBytes = System::IO::File::ReadAllBytes(get_MyDir() + u"morzal.pfx");
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> cert = Aspose::Words::DigitalSignatures::CertificateHolder::Create(certBytes, u"aw");
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(get_MyDir() + u"Digitally signed.docx", get_ArtifactsDir() + u"DigitalSignatureUtil.docx", cert, signOptions);

auto signedDoc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DigitalSignatureUtil.docx");

System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignature> signature = signedDoc->get_DigitalSignatures()->idx_get(0);
ASSERT_EQ(1, signedDoc->get_DigitalSignatures()->get_Count());
ASSERT_TRUE(signature->get_IsValid());
ASSERT_EQ(u"10.0", signature->get_WindowsVersion());
ASSERT_EQ(u"16.0.19127", signature->get_ApplicationVersion());
ASSERT_EQ(u"16.0.19127/27", signature->get_OfficeVersion());
ASSERT_EQ(1024, signature->get_HorizontalResolution());
ASSERT_EQ(768, signature->get_VerticalResolution());
ASSERT_EQ(24, signature->get_ColorDepth());
```

## انظر أيضًا

* Class [CertificateHolder](../../certificateholder/)
* Class [SignOptions](../../signoptions/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::Sign(std::basic_istream\<CharType, Traits\>\&, std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>) method




```cpp
template<typename CharType,typename Traits> static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(std::basic_istream<CharType, Traits> &srcStream, std::basic_ostream<CharType, Traits> &dstStream, System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certHolder)
```

## انظر أيضًا

* Class [CertificateHolder](../../certificateholder/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::Sign(std::basic_istream\<CharType, Traits\>\&, std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>, System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>) method




```cpp
template<typename CharType,typename Traits> static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(std::basic_istream<CharType, Traits> &srcStream, std::basic_ostream<CharType, Traits> &dstStream, System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certHolder, System::SharedPtr<Aspose::Words::DigitalSignatures::SignOptions> signOptions)
```

## انظر أيضًا

* Class [CertificateHolder](../../certificateholder/)
* Class [SignOptions](../../signoptions/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
