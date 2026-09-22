---
title: "Aspose::Words::Saving::PdfEncryptionDetails class"
linktitle: "PdfEncryptionDetails"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::PdfEncryptionDetails sınıfı. PDF belgesi için şifreleme ve erişim izinleriyle ilgili ayrıntıları içerir. Daha fazla bilgi için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 24000
url: /tr/cpp/aspose.words.saving/pdfencryptiondetails/
---
## PdfEncryptionDetails class


Bir PDF belgesi için şifreleme ve erişim izinleri ayrıntılarını içerir. Daha fazla bilgi için, [Bir Belgeyi Korumak veya Şifrelemek](https://docs.aspose.com/words/cpp/protect-or-encrypt-a-document/) dokümantasyon makalesini ziyaret edin.

```cpp
class PdfEncryptionDetails : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_OwnerPassword](./get_ownerpassword/)() const | Şifrelenmiş PDF belgesi için sahibi parolasını belirtir. |
| [get_Permissions](./get_permissions/)() const | Şifrelenmiş bir PDF belgesinde bir kullanıcıya izin verilen işlemleri belirtir. Varsayılan değer [DisallowAll](../pdfpermissions/). |
| [get_UserPassword](./get_userpassword/)() const | Şifrelenmiş PDF belgesini açmak için gereken kullanıcı parolasını belirtir. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PdfEncryptionDetails](./pdfencryptiondetails/)(const System::String\&, const System::String\&) | Bu sınıfın bir örneğini başlatır. |
| [PdfEncryptionDetails](./pdfencryptiondetails/)(const System::String\&, const System::String\&, Aspose::Words::Saving::PdfPermissions) | Bu sınıfın bir örneğini başlatır. |
| [set_OwnerPassword](./set_ownerpassword/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Saving::PdfEncryptionDetails::get_OwnerPassword](./get_ownerpassword/). |
| [set_Permissions](./set_permissions/)(Aspose::Words::Saving::PdfPermissions) | Şifrelenmiş bir PDF belgesinde bir kullanıcıya izin verilen işlemleri belirtir. Varsayılan değer [DisallowAll](../pdfpermissions/). |
| [set_UserPassword](./set_userpassword/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Saving::PdfEncryptionDetails::get_UserPassword](./get_userpassword/). |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
