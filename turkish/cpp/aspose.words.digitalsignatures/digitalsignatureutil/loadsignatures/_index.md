---
title: "Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures method"
linktitle: "LoadSignatures"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures yöntemi. C++'ta akış kullanarak belgeden dijital imzaları yükler."
type: docs
weight: 1000
url: /tr/cpp/aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/
---
## DigitalSignatureUtil::LoadSignatures(const System::SharedPtr\<System::IO::Stream\>\&) method


Akış kullanarak belgeden dijital imzaları yükler.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| akış | const System::SharedPtr\<System::IO::Stream\>\& | Belge içeren akış. |

### ReturnValue

Dijital imzaların koleksiyonu. Dosya imzalanmamışsa boş koleksiyon döndürür.

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

## Ayrıca Bakınız

* Class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::LoadSignatures(const System::String\&) method


Belgeden dijital imzaları yükler.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(const System::String &fileName)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | const System::String\& | Belgeye giden yol. |

### ReturnValue

Dijital imzaların koleksiyonu. Dosya imzalanmamışsa boş koleksiyon döndürür.

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

* Class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::LoadSignatures(std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> static System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(std::basic_istream<CharType, Traits> &stream)
```

## Ayrıca Bakınız

* Class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
