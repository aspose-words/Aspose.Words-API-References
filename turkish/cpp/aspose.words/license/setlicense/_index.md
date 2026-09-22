---
title: "Aspose::Words::License::SetLicense metodu"
linktitle: "SetLicense"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::License::SetLicense metodu. Bileşeni C++'da lisanslar."
type: docs
weight: 5000
url: /tr/cpp/aspose.words/license/setlicense/
---
## License::SetLicense(const System::SharedPtr\<System::IO::Stream\>\&) method


Bileşeni lisanslar.

```cpp
void Aspose::Words::License::SetLicense(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| akış | const System::SharedPtr\<System::IO::Stream\>\& | Lisansı içeren bir akış. |
## Açıklamalar


Bu metodu bir akıştan lisans yüklemek için kullanın.

## Örnekler



Bir akıştan Aspose.Words için lisans başlatmanın nasıl yapılacağını gösterir.
```cpp
System::String testLicenseFileName = u"Aspose.Words.Cpp.lic";
// Yerel dosya sistemimizdeki geçerli bir lisans dosyası için bir akış geçirerek Aspose.Words ürünümüzün lisansını ayarlayın.
{
    System::SharedPtr<System::IO::Stream> myStream = System::IO::File::OpenRead(System::IO::Path::Combine(get_LicenseDir(), testLicenseFileName));
    auto license = System::MakeObject<Aspose::Words::License>();
    license->SetLicense(myStream);
}
```

## Ayrıca Bakınız

* Class [License](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## License::SetLicense(const System::String\&) method


Bileşeni lisanslar.

```cpp
void Aspose::Words::License::SetLicense(const System::String &licenseName)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| licenseName | const System::String\& | Tam veya kısa bir dosya adı olabilir. Değerlendirme moduna geçmek için boş bir dize kullanın. |
## Açıklamalar


Lisansı aşağıdaki konumlarda bulmaya çalışır:

1. Açık yol.
1. Aspose.Words kütüphanesini içeren klasör.
1. İstemcinin uygulamasını içeren klasör.



## Örnekler



Aspose.Words için yerel dosya sistemindeki bir lisans dosyası kullanarak lisansın nasıl başlatılacağını gösterir.
```cpp
System::String testLicenseFileName = u"Aspose.Words.Cpp.lic";

// Geçerli bir lisans dosyasının yerel dosya sistemi dosya adını geçirerek Aspose.Words ürünümüz için lisansı ayarlayın.
System::String licenseFileName = System::IO::Path::Combine(get_LicenseDir(), testLicenseFileName);

auto license = System::MakeObject<Aspose::Words::License>();
license->SetLicense(licenseFileName);

// Uygulamamızın binaries klasöründe lisans dosyamızın bir kopyasını oluşturun.
System::String licenseCopyFileName = System::IO::Path::Combine(get_AssemblyDir(), testLicenseFileName);
System::IO::File::Copy(licenseFileName, licenseCopyFileName);

// Eğer bir dosyanın adını yol olmadan geçirirsek,
// SetLicense, bu dosya için birkaç yerel dosya sistemi konumunu arayacaktır.
// Bu konumlardan biri, lisans dosyamızın bir kopyasını içeren "bin" klasörü olacaktır.
license->SetLicense(testLicenseFileName);
```

## Ayrıca Bakınız

* Class [License](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## License::SetLicense(std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::License::SetLicense(std::basic_istream<CharType, Traits> &stream)
```

## Ayrıca Bakınız

* Class [License](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
