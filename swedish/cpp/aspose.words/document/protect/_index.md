---
title: "Aspose::Words::Document::Protect metod"
linktitle: "Skydda"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::Protect metod. Skyddar dokumentet mot ändringar utan att ändra det befintliga lösenordet eller tilldelar ett slumpmässigt lösenord i C++."
type: docs
weight: 67000
url: /sv/cpp/aspose.words/document/protect/
---
## Document::Protect(Aspose::Words::ProtectionType) method


Skyddar dokumentet mot ändringar utan att ändra det befintliga lösenordet eller tilldelar ett slumpmässigt lösenord.

```cpp
void Aspose::Words::Document::Protect(Aspose::Words::ProtectionType type)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| typ | Aspose::Words::ProtectionType | Anger skyddstypen för dokumentet. |
## Anmärkningar


När ett dokument är skyddat kan användaren bara göra begränsade ändringar, såsom att lägga till kommentarer, göra revisioner eller fylla i ett formulär.

När du skyddar ett dokument och dokumentet redan har ett skyddslösenord ändras inte det befintliga skyddslösenordet.

När du skyddar ett dokument och dokumentet inte har något skyddslösenord tilldelar den här metoden ett slumpmässigt lösenord som gör det omöjligt att avskydda dokumentet i Microsoft Word, men du kan fortfarande avskydda dokumentet i Aspose.Words eftersom det inte kräver ett lösenord vid avskyddning.

## Exempel



Visar hur man stänger av skydd för ett avsnitt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Section 1. Hello world!");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

builder->Writeln(u"Section 2. Hello again!");
builder->Write(u"Please enter text here: ");
builder->InsertTextInput(u"TextInput1", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Placeholder text", 0);

// Applicera skrivskydd på varje avsnitt i dokumentet.
doc->Protect(Aspose::Words::ProtectionType::AllowOnlyFormFields);

// Stäng av skrivskydd för det första avsnittet.
doc->get_Sections()->idx_get(0)->set_ProtectedForForms(false);

// I detta utdata-dokument kommer vi att kunna redigera det första avsnittet fritt,
// och vi kommer endast att kunna redigera innehållet i formulärfältet i det andra avsnittet.
doc->Save(get_ArtifactsDir() + u"Section.Protect.docx");
```

## Se även

* Enum [ProtectionType](../../protectiontype/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Protect(Aspose::Words::ProtectionType, const System::String\&) method


Skyddar dokumentet mot ändringar och kan valfritt ange ett skyddslösenord.

```cpp
void Aspose::Words::Document::Protect(Aspose::Words::ProtectionType type, const System::String &password)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| typ | Aspose::Words::ProtectionType | Anger skyddstypen för dokumentet. |
| password | const System::String\& | Lösenordet att skydda dokumentet med. Ange **null** eller en tom sträng om du vill skydda dokumentet utan lösenord. |
## Anmärkningar


När ett dokument är skyddat kan användaren bara göra begränsade ändringar, såsom att lägga till kommentarer, göra revisioner eller fylla i ett formulär.

Observera att dokumentskydd är annorlunda än skrivskydd. Skrivskydd anges med hjälp av [WriteProtection](../get_writeprotection/).

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
