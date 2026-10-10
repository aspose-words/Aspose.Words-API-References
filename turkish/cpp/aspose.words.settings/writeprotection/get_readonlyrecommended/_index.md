---
title: "Aspose::Words::Settings::WriteProtection::get_ReadOnlyRecommended metodu"
linktitle: "get_ReadOnlyRecommended"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Settings::WriteProtection::get_ReadOnlyRecommended yöntemi. Belge yazarının, belgenin C++'ta yalnızca okunur olarak açılmasını önerip önermediğini belirtir."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.settings/writeprotection/get_readonlyrecommended/
---
## WriteProtection::get_ReadOnlyRecommended method


Belge yazarının, belgenin yalnızca okunur olarak açılmasını önerip önermediğini belirtir.

```cpp
bool Aspose::Words::Settings::WriteProtection::get_ReadOnlyRecommended() const
```


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
