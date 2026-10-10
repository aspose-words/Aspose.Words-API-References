---
title: "Aspose::Words::Document::Protect yöntemi"
linktitle: "Koruma"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::Protect yöntemi. C++'ta mevcut şifreyi değiştirmeden belgeyi değişikliklerden korur veya rastgele bir şifre atar."
type: docs
weight: 67000
url: /tr/cpp/aspose.words/document/protect/
---
## Document::Protect(Aspose::Words::ProtectionType) method


Mevcut şifreyi değiştirmeden belgeyi değişikliklerden korur veya rastgele bir şifre atar.

```cpp
void Aspose::Words::Document::Protect(Aspose::Words::ProtectionType type)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| tür | Aspose::Words::ProtectionType | Belge için koruma türünü belirtir. |
## Açıklamalar


Bir belge korunduğunda, kullanıcı yalnızca ek açıklama ekleme, revizyon yapma veya bir form doldurma gibi sınırlı değişiklikler yapabilir.

Bir belgeyi koruduğunuzda ve belge zaten bir koruma parolası içeriyorsa, mevcut koruma parolası değiştirilmez.

Bir belgeyi koruduğunuzda ve belgede koruma parolası yoksa, bu yöntem Microsoft Word'de belgeyi korumasız bırakmayı imkansız kılan rastgele bir parola atar, ancak Aspose.Words'te belgeyi korumasız bırakmak için parola gerekmediğinden yine de korumasız bırakabilirsiniz.

## Örnekler



Bir bölüm için korumayı nasıl kapatacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Section 1. Hello world!");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

builder->Writeln(u"Section 2. Hello again!");
builder->Write(u"Please enter text here: ");
builder->InsertTextInput(u"TextInput1", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Placeholder text", 0);

// Belgedeki her bölüme yazma koruması uygula.
doc->Protect(Aspose::Words::ProtectionType::AllowOnlyFormFields);

// İlk bölüm için yazma korumasını kapat.
doc->get_Sections()->idx_get(0)->set_ProtectedForForms(false);

// Bu çıktı belgesinde, ilk bölümü serbestçe düzenleyebileceğiz,
// ve yalnızca ikinci bölmedeki form alanının içeriğini düzenleyebileceğiz.
doc->Save(get_ArtifactsDir() + u"Section.Protect.docx");
```

## Ayrıca Bakınız

* Enum [ProtectionType](../../protectiontype/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Protect(Aspose::Words::ProtectionType, const System::String\&) method


Belgeyi değişikliklerden korur ve isteğe bağlı olarak bir koruma şifresi ayarlar.

```cpp
void Aspose::Words::Document::Protect(Aspose::Words::ProtectionType type, const System::String &password)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| tür | Aspose::Words::ProtectionType | Belge için koruma türünü belirtir. |
| password | const System::String\& | Belgeyi korumak için kullanılacak parola. Belgeyi parola olmadan korumak istiyorsanız **null** veya boş bir dize belirtin. |
## Açıklamalar


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
