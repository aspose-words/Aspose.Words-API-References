---
title: "Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures metodu"
linktitle: "RemoveAllSignatures"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures metodu. Kaynak akıştaki belgeden tüm dijital imzaları kaldırır ve imzasız belgeyi hedef akışa yazar. Çıktı akışın başlangıcına yazılacak ve akış boyutu içerik uzunluğuna göre güncellenecektir. Dijital imza kaldırma için aşağıdaki formatlar uyumludur: Doc, Dot, Docx, Dotx, Docm, Dotm, Odt, Ott C++'ta."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/
---
## DigitalSignatureUtil::RemoveAllSignatures(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&) method


Belgeden tüm dijital imzaları kaynak akıştan kaldırır ve imzasız belgeyi hedef akışa yazar. **Çıktı akışın başlangıcına yazılacak ve akış boyutu içerik uzunluğuna göre güncellenecektir.**Aşağıdaki formatlar dijital imza kaldırma için uyumludur: [Doc](../../../aspose.words/loadformat/), [Dot](../../../aspose.words/loadformat/), [Docx](../../../aspose.words/loadformat/), [Dotx](../../../aspose.words/loadformat/), [Docm](../../../aspose.words/loadformat/), [Dotm](../../../aspose.words/loadformat/), [Odt](../../../aspose.words/loadformat/), [Ott](../../../aspose.words/loadformat/).

```cpp
static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures(const System::SharedPtr<System::IO::Stream> &srcStream, const System::SharedPtr<System::IO::Stream> &dstStream)
```


## Örnekler



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

* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::RemoveAllSignatures(const System::String\&, const System::String\&) method


Kaynak dosyadan tüm dijital imzaları kaldırır ve imzasız dosyayı hedef dosyaya yazar. Dijital imza kaldırma için aşağıdaki formatlar uyumludur: [Doc](../../../aspose.words/loadformat/), [Dot](../../../aspose.words/loadformat/), [Docx](../../../aspose.words/loadformat/), [Dotx](../../../aspose.words/loadformat/), [Docm](../../../aspose.words/loadformat/), [Dotm](../../../aspose.words/loadformat/), [Odt](../../../aspose.words/loadformat/), [Ott](../../../aspose.words/loadformat/).

```cpp
static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures(const System::String &srcFileName, const System::String &dstFileName)
```


## Örnekler



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

* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::RemoveAllSignatures(std::basic_istream\<CharType, Traits\>\&, std::basic_ostream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures(std::basic_istream<CharType, Traits> &srcStream, std::basic_ostream<CharType, Traits> &dstStream)
```

## Ayrıca Bakınız

* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
