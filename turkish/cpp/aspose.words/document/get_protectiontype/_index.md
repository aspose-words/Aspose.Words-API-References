---
title: "Aspose::Words::Document::get_ProtectionType yöntemi"
linktitle: "get_ProtectionType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::get_ProtectionType yöntemi. C++'ta geçerli aktif belge koruma türünü alır."
type: docs
weight: 44000
url: /tr/cpp/aspose.words/document/get_protectiontype/
---
## Document::get_ProtectionType method


Şu anda etkin olan belge koruma türünü alır.

```cpp
Aspose::Words::ProtectionType Aspose::Words::Document::get_ProtectionType()
```

## Açıklamalar


Bu özellik, mevcut ayarlanmış belge koruma türünü almanıza izin verir. Belge koruma türünü değiştirmek için [Protect()](../) ve [Unprotect](../unprotect/) yöntemlerini kullanın.

Bir belge korunduğunda, kullanıcı yalnızca ek açıklama ekleme, revizyon yapma veya bir form doldurma gibi sınırlı değişiklikler yapabilir.

Belge korumasının yazma korumasından farklı olduğunu unutmayın. Yazma koruması, [WriteProtection](../get_writeprotection/) kullanılarak belirtilir.

## Örnekler



Bir belgenin nasıl korunacağını ve korumasının nasıl kaldırılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
doc->Protect(Aspose::Words::ProtectionType::ReadOnly, u"password");

ASSERT_EQ(Aspose::Words::ProtectionType::ReadOnly, doc->get_ProtectionType());

// Bu belgeyi Microsoft Word ile düzenlemek amacıyla açarsak,
// korumadan geçmek için şifreyi uygulamamız gerekir.
doc->Save(get_ArtifactsDir() + u"Document.Protect.docx");

// Korumanın yalnızca belgemizi Microsoft Word kullanıcıları açtığında geçerli olduğunu unutmayın.
// Belgeyi hiçbir şekilde şifrelemedik ve programlı olarak açıp düzenlemek için şifreye ihtiyacımız yok.
auto protectedDoc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.Protect.docx");

ASSERT_EQ(Aspose::Words::ProtectionType::ReadOnly, protectedDoc->get_ProtectionType());

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(protectedDoc);
builder->Writeln(u"Text added to a protected document.");

// Bir belgenin korumasını kaldırmanın iki yolu vardır.
// 1 - Şifre olmadan:
doc->Unprotect();

ASSERT_EQ(Aspose::Words::ProtectionType::NoProtection, doc->get_ProtectionType());

doc->Protect(Aspose::Words::ProtectionType::ReadOnly, u"NewPassword");

ASSERT_EQ(Aspose::Words::ProtectionType::ReadOnly, doc->get_ProtectionType());

doc->Unprotect(u"WrongPassword");

ASSERT_EQ(Aspose::Words::ProtectionType::ReadOnly, doc->get_ProtectionType());

// 2 - Doğru şifre ile:
doc->Unprotect(u"NewPassword");

ASSERT_EQ(Aspose::Words::ProtectionType::NoProtection, doc->get_ProtectionType());
```

## Ayrıca Bakınız

* Enum [ProtectionType](../../protectiontype/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
