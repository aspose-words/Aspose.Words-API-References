---
title: "Aspose::Words::DigitalSignatures::DigitalSignatureCollection class"
linktitle: "DigitalSignatureCollection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::DigitalSignatures::DigitalSignatureCollection class. يوفر مجموعة للقراءة فقط من التوقيعات الرقمية المرفقة بالمستند. لمعرفة المزيد، زر مقالة التوثيق في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.digitalsignatures/digitalsignaturecollection/
---
## DigitalSignatureCollection class


يوفر مجموعة للقراءة فقط من التوقيعات الرقمية المرفقة بمستند. لمعرفة المزيد، زر مقالة الوثائق [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/).

```cpp
class DigitalSignatureCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignature>>
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [DigitalSignatureCollection](./digitalsignaturecollection/)() |  |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | يحصل على عدد العناصر الموجودة في المجموعة. |
| [get_IsValid](./get_isvalid/)() | يرجع **true** إذا كانت جميع التوقيعات الرقمية في هذه المجموعة صالحة ولم يتم العبث بالمستند. كما يرجع **true** إذا لم تكن هناك أي توقيعات رقمية. يرجع **false** إذا كان هناك توقيع رقمي واحد على الأقل غير صالح. |
| [GetEnumerator](./getenumerator/)() override | يرجع كائن عداد القاموس الذي يمكن استخدامه للتنقل عبر جميع العناصر في المجموعة. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | يحصل على توقيع المستند عند الفهرس المحدد. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| تعريف نوع | الوصف |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |

## أمثلة



يوضح كيفية التحقق من صحة وعرض معلومات كل توقيع في المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Digitally signed.docx");

for (auto&& signature : doc->get_DigitalSignatures())
{
    std::cout << System::String::Format(u"{0} signature: ", (signature->get_IsValid() ? System::String(u"Valid") : System::String(u"Invalid"))) << std::endl;
    std::cout << System::String::Format(u"\tReason:\t{0}", signature->get_Comments()) << std::endl;
    std::cout << System::String::Format(u"\tType:\t{0}", signature->get_SignatureType()) << std::endl;
    std::cout << System::String::Format(u"\tSign time:\t{0}", signature->get_SignTime()) << std::endl;
    std::cout << System::String::Format(u"\tSubject name:\t{0}", signature->get_CertificateHolder()->get_Certificate()->get_SubjectName()) << std::endl;
    std::cout << System::String::Format(u"\tIssuer name:\t{0}", signature->get_CertificateHolder()->get_Certificate()->get_IssuerName()->get_Name()) << std::endl;
    std::cout << std::endl;
}
```


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

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
