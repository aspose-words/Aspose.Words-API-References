---
title: "Aspose::Words::License sınıfı"
linktitle: "License"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::License sınıfı. Bileşeni lisanslamak için yöntemler sağlar. Daha fazla bilgi için C++'taki belge makalesini ziyaret edin."
type: docs
weight: 39000
url: /tr/cpp/aspose.words/license/
---
## License class


Bileşeni lisanslamak için yöntemler sağlar. Daha fazla bilgi edinmek için [Licensing and Subscription](https://docs.aspose.com/words/cpp/licensing/) dokümantasyon makalesini ziyaret edin.

```cpp
class License : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [License](./license/)() | Bu sınıfın yeni bir örneğini başlatır. |
| [SetLicense](./setlicense/)(const System::String\&) | Bileşeni lisanslar. |
| [SetLicense](./setlicense/)(const System::SharedPtr\<System::IO::Stream\>\&) | Bileşeni lisanslar. |
| [SetLicense](./setlicense/)(std::basic_istream\<CharType, Traits\>\&) |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
