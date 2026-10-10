---
title: "Aspose::Words::DigitalSignatures::DigitalSignatureUtil sınıfı"
linktitle: "DigitalSignatureUtil"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DigitalSignatures::DigitalSignatureUtil sınıfı. Belge imzalama yöntemleri sağlar. Daha fazla bilgi için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.digitalsignatures/digitalsignatureutil/
---
## DigitalSignatureUtil class


Belgeyi imzalamak için yöntemler sağlar. Daha fazla bilgi için, [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/) dokümantasyon makalesini ziyaret edin.

```cpp
class DigitalSignatureUtil
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [DigitalSignatureUtil](./digitalsignatureutil/)() |  |
| static [LoadSignatures](./loadsignatures/)(const System::String\&) | Belgeden dijital imzaları yükler. |
| static [LoadSignatures](./loadsignatures/)(const System::SharedPtr\<System::IO::Stream\>\&) | Akış kullanarak belgeden dijital imzaları yükler. |
| static [LoadSignatures](./loadsignatures/)(std::basic_istream\<CharType, Traits\>\&) |  |
| static [RemoveAllSignatures](./removeallsignatures/)(const System::String\&, const System::String\&) | Kaynak dosyadan tüm dijital imzaları kaldırır ve imzasız dosyayı hedef dosyaya yazar. Dijital imza kaldırma için aşağıdaki formatlar uyumludur: [Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/). |
| static [RemoveAllSignatures](./removeallsignatures/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&) | Kaynak akıştaki belgeden tüm dijital imzaları kaldırır ve imzasız belgeyi hedef akışa yazar. **Çıktı akışın başına yazılacak ve akış boyutu içerik uzunluğuna göre güncellenecektir.** Aşağıdaki formatlar dijital imza kaldırma için uyumludur: [Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/). |
| static [RemoveAllSignatures](./removeallsignatures/)(std::basic_istream\<CharType, Traits\>\&, std::basic_ostream\<CharType, Traits\>\&) |  |
| static [Sign](./sign/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | Verilen [CertificateHolder](../certificateholder/) ve [SignOptions](../signoptions/) kullanarak kaynak belgeyi dijital imza ile imzalar ve imzalı belgeyi hedef akışa yazar. Desteklenen formatlar: [Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/).**Çıktı akışın başına yazılacak ve akış boyutu içerik uzunluğuna göre güncellenecektir.** |
| static [Sign](./sign/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | Verilen [CertificateHolder](../certificateholder/) ve [SignOptions](../signoptions/) kullanarak kaynak belgeyi dijital imza ile imzalar ve imzalı belgeyi hedef dosyaya yazar. Desteklenen formatlar: [Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/). |
| static [Sign](./sign/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | Verilen [CertificateHolder](../certificateholder/) kullanarak kaynak belgeyi dijital imza ile imzalar ve imzalı belgeyi hedef akışa yazar. Desteklenen formatlar: [Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/).**Çıktı akışın başına yazılacak ve akış boyutu içerik uzunluğuna göre güncellenecektir.** |
| static [Sign](./sign/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | Verilen [CertificateHolder](../certificateholder/) kullanarak kaynak belgeyi dijital imza ile imzalar ve imzalı belgeyi hedef dosyaya yazar. Desteklenen formatlar: [Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/). |
| static [Sign](./sign/)(std::basic_istream\<CharType, Traits\>\&, std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>, System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>) |  |
| static [Sign](./sign/)(std::basic_istream\<CharType, Traits\>\&, std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>) |  |
## Açıklamalar


Dijital imza dosya içeriğiyle çalıştığı ve [Document](../../aspose.words/document/) Nesne Modeliyle çalışmadığı için bu yöntemler ayrı bir sınıfa konulmuştur.

Desteklenen formatlar şunlardır: [Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/).

## Örnekler



Dijital olarak imzalanmış bir belgeden imzaların nasıl yükleneceğini gösterir.
```cpp
// DigitalSignatureUtil sınıfını kullanarak imzalı bir belgenin dijital imza koleksiyonunu yüklemenin iki yolu vardır.
// 1 -  Yerel dosya sistemindeki bir dosya adıyla bir belgeden yükle:
System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> digitalSignatures = Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(get_MyDir() + u"Digitally signed.docx");

// Bu koleksiyon boş değilse, belgenin dijital olarak imzalı olduğunu doğrulayabiliriz.
ASSERT_EQ(1, digitalSignatures->get_Count());

// 2 -  Bir FileStream'den belge yükle:
{
    System::SharedPtr<System::IO::Stream> stream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Digitally signed.docx", System::IO::FileMode::Open);
    digitalSignatures = Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(stream);
    ASSERT_EQ(1, digitalSignatures->get_Count());
}
```


Dijital olarak imzalanmış bir belgeden dijital imzaların nasıl kaldırılacağını gösterir.
```cpp
// DigitalSignatureUtil sınıfını kullanarak dijital imzaları kaldırmanın iki yolu vardır
// İmzalı bir belgeden, yerel dosya sisteminde başka bir yere imzasız bir kopyasını kaydederek.
// 1 -  İmzalı belge ve imzasız kopyanın konumlarını dosya adı dizgileriyle belirleyin:
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures(get_MyDir() + u"Digitally signed.docx", get_ArtifactsDir() + u"DigitalSignatureUtil.LoadAndRemove.FromString.docx");

// 2 -  İmzalı belge ve imzasız kopyanın konumlarını dosya akışlarıyla belirleyin:
{
    System::SharedPtr<System::IO::Stream> streamIn = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Digitally signed.docx", System::IO::FileMode::Open);
    {
        System::SharedPtr<System::IO::Stream> streamOut = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"DigitalSignatureUtil.LoadAndRemove.FromStream.docx", System::IO::FileMode::Create);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures(streamIn, streamOut);
    }
}

// Her iki çıktı belgemizin de dijital imza içermediğini doğrulayın.
ASSERT_EQ(0, Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(get_ArtifactsDir() + u"DigitalSignatureUtil.LoadAndRemove.FromString.docx")->get_Count());
ASSERT_EQ(0, Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(get_ArtifactsDir() + u"DigitalSignatureUtil.LoadAndRemove.FromStream.docx")->get_Count());
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
