---
title: "Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign metodu"
linktitle: "Sign"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign metodu. Verilen CertificateHolder ile dijital imza kullanarak kaynak belgeyi imzalar ve imzalı belgeyi hedef akışa yazar. Desteklenen formatlar: Doc, Dot, Docx, Dotx, Docm, Dotm, Odt, Ott. Çıktı akışın başlangıcına yazılacak ve akış boyutu içerik uzunluğuna göre güncellenecektir C++'ta."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.digitalsignatures/digitalsignatureutil/sign/
---
## DigitalSignatureUtil::Sign(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) method


Verilen [CertificateHolder](../../certificateholder/) ile dijital imza kullanarak kaynak belgeyi imzalar ve imzalı belgeyi hedef akışa yazar. Desteklenen formatlar: [Doc](../../../aspose.words/loadformat/), [Dot](../../../aspose.words/loadformat/), [Docx](../../../aspose.words/loadformat/), [Dotx](../../../aspose.words/loadformat/), [Docm](../../../aspose.words/loadformat/), [Dotm](../../../aspose.words/loadformat/), [Odt](../../../aspose.words/loadformat/), [Ott](../../../aspose.words/loadformat/).**Çıktı akışın başlangıcına yazılacak ve akış boyutu içerik uzunluğuna göre güncellenecektir.**

```cpp
static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(const System::SharedPtr<System::IO::Stream> &srcStream, const System::SharedPtr<System::IO::Stream> &dstStream, const System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> &certHolder)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| srcStream | const System::SharedPtr\<System::IO::Stream\>\& | İmzalanacak belgeyi içeren akış. |
| dstStream | const System::SharedPtr\<System::IO::Stream\>\& | İmzalı belgenin yazılacağı akış. |
| certHolder | const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\& | [CertificateHolder](../../certificateholder/) nesnesi, dosyayı imzalamak için kullanılan sertifikayı içerir. Tutucudaki sertifika ZORUNLU olarak özel anahtarlar içermelidir. |

## Örnekler



X.509 sertifikalarıyla belgelerin nasıl imzalanacağını gösterir.
```cpp
// Belgenin imzalanmadığını doğrulayın.
ASSERT_FALSE(Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.docx")->get_HasDigitalSignature());

// Belgeyi imzalamak için kullanacağımız bir PKCS12 dosyasından CertificateHolder nesnesi oluşturun.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw", nullptr);

// Yerel dosya sistemine imzalı bir belge kopyası kaydetmenin iki yolu vardır:
// 1 - Belgeyi yerel sistem dosya adıyla belirleyin ve imzalı bir kopyayı başka bir dosya adıyla belirtilen konuma kaydedin.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_SignTime(System::DateTime::get_Now());
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(get_MyDir() + u"Document.docx", get_ArtifactsDir() + u"Document.DigitalSignature.docx", certificateHolder, signOptions);

ASSERT_TRUE(Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"Document.DigitalSignature.docx")->get_HasDigitalSignature());

// 2 - Belgeyi bir akıştan alın ve imzalı bir kopyayı başka bir akışa kaydedin.
{
    auto inDoc = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Document.docx", System::IO::FileMode::Open);
    {
        auto outDoc = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"Document.DigitalSignature.docx", System::IO::FileMode::Create);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inDoc, outDoc, certificateHolder);
    }
}

ASSERT_TRUE(Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"Document.DigitalSignature.docx")->get_HasDigitalSignature());

// Lütfen belgenin tüm dijital imzalarının geçerli olduğunu doğrulayın ve ayrıntılarını kontrol edin.
auto signedDoc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.DigitalSignature.docx");
System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> digitalSignatureCollection = signedDoc->get_DigitalSignatures();

ASSERT_TRUE(digitalSignatureCollection->get_IsValid());
ASSERT_EQ(1, digitalSignatureCollection->get_Count());
ASSERT_EQ(Aspose::Words::DigitalSignatures::DigitalSignatureType::XmlDsig, digitalSignatureCollection->idx_get(0)->get_SignatureType());
ASSERT_EQ(u"CN=Morzal.Me", signedDoc->get_DigitalSignatures()->idx_get(0)->get_IssuerName());
ASSERT_EQ(u"CN=Morzal.Me", signedDoc->get_DigitalSignatures()->idx_get(0)->get_SubjectName());
```

## Ayrıca Bakınız

* Class [CertificateHolder](../../certificateholder/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::Sign(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) method


Verilen [CertificateHolder](../../certificateholder/) ve [SignOptions](../../signoptions/) kullanarak kaynak belgeyi dijital imza ile imzalar ve imzalı belgeyi hedef akışa yazar. Desteklenen formatlar: [Doc](../../../aspose.words/loadformat/), [Dot](../../../aspose.words/loadformat/), [Docx](../../../aspose.words/loadformat/), [Dotx](../../../aspose.words/loadformat/), [Docm](../../../aspose.words/loadformat/), [Dotm](../../../aspose.words/loadformat/), [Odt](../../../aspose.words/loadformat/), [Ott](../../../aspose.words/loadformat/).**Çıktı akışın başına yazılacak ve akış boyutu içerik uzunluğuna göre güncellenecektir.**

```cpp
static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(const System::SharedPtr<System::IO::Stream> &srcStream, const System::SharedPtr<System::IO::Stream> &dstStream, const System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> &certHolder, const System::SharedPtr<Aspose::Words::DigitalSignatures::SignOptions> &signOptions)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| srcStream | const System::SharedPtr\<System::IO::Stream\>\& | İmzalanacak belgeyi içeren akış. |
| dstStream | const System::SharedPtr\<System::IO::Stream\>\& | İmzalı belgenin yazılacağı akış. |
| certHolder | const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\& | [CertificateHolder](../../certificateholder/) nesnesi, dosyayı imzalamak için kullanılan sertifikayı içerir. Tutucudaki sertifika ZORUNLU olarak özel anahtarlar içermelidir. |
| signOptions | const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\& | [SignOptions](../../signoptions/) nesnesi çeşitli imzalama seçenekleriyle. |

## Örnekler



Belgeleri dijital olarak imzalamanın nasıl yapılacağını gösterir.
```cpp
// Özel anahtar içermesi gereken bir PKCS#12 deposundan X.509 sertifikası oluşturun.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

// Yeni dijital imzamızla uygulanacak bir yorum ve tarih oluşturun.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"My comment");
signOptions->set_SignTime(System::DateTime::get_Now());

// Yerel dosya sisteminden bir dosya akışı aracılığıyla imzasız bir belge alın,
// daha sonra çıktı dosya akışının dosya adıyla belirlenen imzalı bir kopyasını oluşturun.
{
    System::SharedPtr<System::IO::Stream> streamIn = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Document.docx", System::IO::FileMode::Open);
    {
        System::SharedPtr<System::IO::Stream> streamOut = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"DigitalSignatureUtil.SignDocument.docx", System::IO::FileMode::OpenOrCreate);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

## Ayrıca Bakınız

* Class [CertificateHolder](../../certificateholder/)
* Class [SignOptions](../../signoptions/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::Sign(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) method


Verilen [CertificateHolder](../../certificateholder/) kullanarak kaynak belgeyi dijital imza ile imzalar ve imzalı belgeyi hedef dosyaya yazar. Desteklenen formatlar: [Doc](../../../aspose.words/loadformat/), [Dot](../../../aspose.words/loadformat/), [Docx](../../../aspose.words/loadformat/), [Dotx](../../../aspose.words/loadformat/), [Docm](../../../aspose.words/loadformat/), [Dotm](../../../aspose.words/loadformat/), [Odt](../../../aspose.words/loadformat/), [Ott](../../../aspose.words/loadformat/).

```cpp
static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(const System::String &srcFileName, const System::String &dstFileName, const System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> &certHolder)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| srcFileName | const System::String\& | İmzalanacak belgenin dosya adı. |
| dstFileName | const System::String\& | İmzalı belgenin çıktı dosya adı. |
| certHolder | const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\& | [CertificateHolder](../../certificateholder/) nesnesi, dosyayı imzalamak için kullanılan sertifikayı içerir. Tutucudaki sertifika ZORUNLU olarak özel anahtarlar içermelidir. |

## Örnekler



X.509 sertifikalarıyla belgelerin nasıl imzalanacağını gösterir.
```cpp
// Belgenin imzalanmadığını doğrulayın.
ASSERT_FALSE(Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.docx")->get_HasDigitalSignature());

// Belgeyi imzalamak için kullanacağımız bir PKCS12 dosyasından CertificateHolder nesnesi oluşturun.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw", nullptr);

// Yerel dosya sistemine imzalı bir belge kopyası kaydetmenin iki yolu vardır:
// 1 - Belgeyi yerel sistem dosya adıyla belirleyin ve imzalı bir kopyayı başka bir dosya adıyla belirtilen konuma kaydedin.
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_SignTime(System::DateTime::get_Now());
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(get_MyDir() + u"Document.docx", get_ArtifactsDir() + u"Document.DigitalSignature.docx", certificateHolder, signOptions);

ASSERT_TRUE(Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"Document.DigitalSignature.docx")->get_HasDigitalSignature());

// 2 - Belgeyi bir akıştan alın ve imzalı bir kopyayı başka bir akışa kaydedin.
{
    auto inDoc = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Document.docx", System::IO::FileMode::Open);
    {
        auto outDoc = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"Document.DigitalSignature.docx", System::IO::FileMode::Create);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inDoc, outDoc, certificateHolder);
    }
}

ASSERT_TRUE(Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"Document.DigitalSignature.docx")->get_HasDigitalSignature());

// Lütfen belgenin tüm dijital imzalarının geçerli olduğunu doğrulayın ve ayrıntılarını kontrol edin.
auto signedDoc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.DigitalSignature.docx");
System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> digitalSignatureCollection = signedDoc->get_DigitalSignatures();

ASSERT_TRUE(digitalSignatureCollection->get_IsValid());
ASSERT_EQ(1, digitalSignatureCollection->get_Count());
ASSERT_EQ(Aspose::Words::DigitalSignatures::DigitalSignatureType::XmlDsig, digitalSignatureCollection->idx_get(0)->get_SignatureType());
ASSERT_EQ(u"CN=Morzal.Me", signedDoc->get_DigitalSignatures()->idx_get(0)->get_IssuerName());
ASSERT_EQ(u"CN=Morzal.Me", signedDoc->get_DigitalSignatures()->idx_get(0)->get_SubjectName());
```

## Ayrıca Bakınız

* Class [CertificateHolder](../../certificateholder/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::Sign(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) method


Verilen [CertificateHolder](../../certificateholder/) ve [SignOptions](../../signoptions/) kullanarak kaynak belgeyi dijital imza ile imzalar ve imzalı belgeyi hedef dosyaya yazar. Desteklenen formatlar: [Doc](../../../aspose.words/loadformat/), [Dot](../../../aspose.words/loadformat/), [Docx](../../../aspose.words/loadformat/), [Dotx](../../../aspose.words/loadformat/), [Docm](../../../aspose.words/loadformat/), [Dotm](../../../aspose.words/loadformat/), [Odt](../../../aspose.words/loadformat/), [Ott](../../../aspose.words/loadformat/).

```cpp
static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(const System::String &srcFileName, const System::String &dstFileName, const System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> &certHolder, const System::SharedPtr<Aspose::Words::DigitalSignatures::SignOptions> &signOptions)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| srcFileName | const System::String\& | İmzalanacak belgenin dosya adı. |
| dstFileName | const System::String\& | İmzalı belgenin çıktı dosya adı. |
| certHolder | const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\& | [CertificateHolder](../../certificateholder/) nesnesi, dosyayı imzalamak için kullanılan sertifikayı içerir. Tutucudaki sertifika ZORUNLU olarak özel anahtarlar içermelidir. |
| signOptions | const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\& | [SignOptions](../../signoptions/) nesnesi çeşitli imzalama seçenekleriyle. |

## Örnekler



Ek imzalama seçenekleriyle bir belgeyi nasıl imzalayacağınızı gösterir.
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

## Ayrıca Bakınız

* Class [CertificateHolder](../../certificateholder/)
* Class [SignOptions](../../signoptions/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::Sign(std::basic_istream\<CharType, Traits\>\&, std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>) method




```cpp
template<typename CharType,typename Traits> static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(std::basic_istream<CharType, Traits> &srcStream, std::basic_ostream<CharType, Traits> &dstStream, System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certHolder)
```

## Ayrıca Bakınız

* Class [CertificateHolder](../../certificateholder/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::Sign(std::basic_istream\<CharType, Traits\>\&, std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>, System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>) method




```cpp
template<typename CharType,typename Traits> static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(std::basic_istream<CharType, Traits> &srcStream, std::basic_ostream<CharType, Traits> &dstStream, System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certHolder, System::SharedPtr<Aspose::Words::DigitalSignatures::SignOptions> signOptions)
```

## Ayrıca Bakınız

* Class [CertificateHolder](../../certificateholder/)
* Class [SignOptions](../../signoptions/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
