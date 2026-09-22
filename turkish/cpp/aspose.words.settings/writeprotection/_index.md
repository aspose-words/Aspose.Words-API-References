---
title: "Aspose::Words::Settings::WriteProtection sınıfı"
linktitle: "WriteProtection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Settings::WriteProtection sınıfı. Bir belge için yazma koruması ayarlarını belirtir. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 10000
url: /tr/cpp/aspose.words.settings/writeprotection/
---
## WriteProtection class


Bir belge için yazma koruma ayarlarını belirtir. Daha fazla bilgi için, [Protect or Encrypt a Document](https://docs.aspose.com/words/cpp/protect-or-encrypt-a-document/) dokümantasyon makalesini ziyaret edin.

```cpp
class WriteProtection : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_IsWriteProtected](./get_iswriteprotected/)() | Yazma koruması parolası ayarlandığında **true** döndürür. |
| [get_ReadOnlyRecommended](./get_readonlyrecommended/)() const | Belge yazarının, belgenin yalnızca okunur olarak açılmasını önerip önermediğini belirtir. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ReadOnlyRecommended](./set_readonlyrecommended/)(bool) | Ayarlayıcı: [Aspose::Words::Settings::WriteProtection::get_ReadOnlyRecommended](./get_readonlyrecommended/). |
| [SetPassword](./setpassword/)(const System::String\&) | Belge için yazma koruması parolasını ayarlar. |
| static [Type](./type/)() |  |
| [ValidatePassword](./validatepassword/)(const System::String\&) | Belirtilen parola, belgenin korunduğu yazma koruma parolasıyla aynıysa **true** döndürür. Belge parola ile korunmuyorsa **false** döndürür. |
## Açıklamalar


Yazma koruması, yazarın belgenin yalnızca okunur olarak açılmasını önerip önermediğini ve/veya belgeyi değiştirmek için bir parola gerekip gerekmediğini belirtir.

Yazma koruması, belge korumasından farklıdır. Yazma koruması, Microsoft Word'de 'Farklı Kaydet' iletişim kutusunun seçeneklerinde belirtilir.

Bu sınıfın örneklerini doğrudan oluşturmazsınız. Belge koruma ayarlarına [WriteProtection](../../aspose.words/document/get_writeprotection/) özelliği aracılığıyla erişirsiniz.

## Örnekler



Bir belgeyi şifreyle korumanın nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world! This document is protected.");

// 15 karaktere kadar bir şifre girin ve ardından belgenin koruma durumunu doğrulayın.
doc->get_WriteProtection()->SetPassword(u"MyPassword");
doc->get_WriteProtection()->set_ReadOnlyRecommended(true);

ASSERT_TRUE(doc->get_WriteProtection()->get_IsWriteProtected());
ASSERT_TRUE(doc->get_WriteProtection()->ValidatePassword(u"MyPassword"));

// Korumalar, belgenin programlı olarak düzenlenmesini engellemez ve içeriği şifrelemez.
doc->Save(get_ArtifactsDir() + u"Document.WriteProtection.docx");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.WriteProtection.docx");

ASSERT_TRUE(doc->get_WriteProtection()->get_IsWriteProtected());

builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->Writeln(u"Writing text in a protected document.");

ASSERT_EQ(System::String(u"Hello world! This document is protected.") + u"\rWriting text in a protected document.", doc->GetText().Trim());
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
