---
title: "Aspose::Words::Document::get_ProtectionType metod"
linktitle: "get_ProtectionType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::get_ProtectionType metod. Hämtar den för närvarande aktiva dokumentskyddstypen i C++."
type: docs
weight: 44000
url: /sv/cpp/aspose.words/document/get_protectiontype/
---
## Document::get_ProtectionType method


Hämtar den för närvarande aktiva dokumentskyddstypen.

```cpp
Aspose::Words::ProtectionType Aspose::Words::Document::get_ProtectionType()
```

## Anmärkningar


Denna egenskap möjliggör att hämta den för närvarande inställda dokumentskyddstypen. För att ändra dokumentskyddstypen använd [Protect()](../) och [Unprotect](../unprotect/) metoderna.

När ett dokument är skyddat kan användaren bara göra begränsade ändringar, såsom att lägga till kommentarer, göra revisioner eller fylla i ett formulär.

Observera att dokumentskydd är annorlunda än skrivskydd. Skrivskydd specificeras med hjälp av [WriteProtection](../get_writeprotection/)

## Exempel



Visar hur man skyddar och avskyddar ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
doc->Protect(Aspose::Words::ProtectionType::ReadOnly, u"password");

ASSERT_EQ(Aspose::Words::ProtectionType::ReadOnly, doc->get_ProtectionType());

// Om vi öppnar detta dokument med Microsoft Word med avsikt att redigera det,
// behöver vi ange lösenordet för att komma förbi skyddet.
doc->Save(get_ArtifactsDir() + u"Document.Protect.docx");

// Observera att skyddet endast gäller för Microsoft Word‑användare som öppnar vårt dokument.
// Vi har inte krypterat dokumentet på något sätt, och vi behöver inte lösenordet för att öppna och redigera det programmässigt.
auto protectedDoc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.Protect.docx");

ASSERT_EQ(Aspose::Words::ProtectionType::ReadOnly, protectedDoc->get_ProtectionType());

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(protectedDoc);
builder->Writeln(u"Text added to a protected document.");

// Det finns två sätt att ta bort skydd från ett dokument.
// 1 - Utan lösenord:
doc->Unprotect();

ASSERT_EQ(Aspose::Words::ProtectionType::NoProtection, doc->get_ProtectionType());

doc->Protect(Aspose::Words::ProtectionType::ReadOnly, u"NewPassword");

ASSERT_EQ(Aspose::Words::ProtectionType::ReadOnly, doc->get_ProtectionType());

doc->Unprotect(u"WrongPassword");

ASSERT_EQ(Aspose::Words::ProtectionType::ReadOnly, doc->get_ProtectionType());

// 2 - Med rätt lösenord:
doc->Unprotect(u"NewPassword");

ASSERT_EQ(Aspose::Words::ProtectionType::NoProtection, doc->get_ProtectionType());
```

## Se även

* Enum [ProtectionType](../../protectiontype/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
