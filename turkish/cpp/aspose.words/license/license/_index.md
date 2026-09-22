---
title: "Aspose::Words::License::License yapıcı"
linktitle: "License"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::License::License yapıcı. Bu sınıfın yeni bir örneğini C++'ta başlatır."
type: docs
weight: 2000
url: /tr/cpp/aspose.words/license/license/
---
## License::License constructor


Bu sınıfın yeni bir örneğini başlatır.

```cpp
Aspose::Words::License::License()
```


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
