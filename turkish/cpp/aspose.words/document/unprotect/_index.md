---
title: "Aspose::Words::Document::Unprotect yöntemi"
linktitle: "Korumayı Kaldır"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::Unprotect yöntemi. Belgeyi, şifre ne olursa olsun, C++ içinde korumayı kaldırır."
type: docs
weight: 95000
url: /tr/cpp/aspose.words/document/unprotect/
---
## Document::Unprotect() method


Parola ne olursa olsun belgenin korumasını kaldırır.

```cpp
void Aspose::Words::Document::Unprotect()
```

## Açıklamalar


Bu yöntem, belge bir koruma şifresi taşısa bile korumayı kaldırır.

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Unprotect(const System::String\&) method


Doğru bir parola belirtilirse belgenin korumasını kaldırır.

```cpp
bool Aspose::Words::Document::Unprotect(const System::String &password)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| password | const System::String\& | Belgenin korumasını kaldırmak için kullanılacak şifre. |

### ReturnValue

**true** if a correct password was specified and the document was unprotected.
## Açıklamalar


Bu yöntem, yalnızca doğru bir şifre belirtildiğinde belgenin korumasını kaldırır.

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
