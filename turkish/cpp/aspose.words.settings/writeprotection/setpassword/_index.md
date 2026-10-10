---
title: "Aspose::Words::Settings::WriteProtection::SetPassword yöntemi"
linktitle: "SetPassword"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Settings::WriteProtection::SetPassword yöntemi. Belge için yazma koruma şifresini C++'ta ayarlar."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.settings/writeprotection/setpassword/
---
## WriteProtection::SetPassword method


Belge için yazma koruması parolasını ayarlar.

```cpp
void Aspose::Words::Settings::WriteProtection::SetPassword(const System::String &password)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| password | const System::String\& | Ayarlanacak şifre. **null** olamaz, ancak boş bir dize olabilir. |
## Açıklamalar


Bir şifre ayarlanırsa, Microsoft Word kullanıcıdan şifreyi girmesini isteyecek veya belgeyi yalnızca okunur olarak açacaktır.

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

* Class [WriteProtection](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
