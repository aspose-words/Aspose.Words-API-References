---
title: "Aspose::Words::Document::Unprotect metod"
linktitle: "Unprotect"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Document::Unprotect metod. Tar bort skyddet från dokumentet oavsett lösenord i C++."
type: docs
weight: 95000
url: /sv/cpp/aspose.words/document/unprotect/
---
## Document::Unprotect() method


Tar bort skyddet från dokumentet oavsett lösenord.

```cpp
void Aspose::Words::Document::Unprotect()
```

## Anmärkningar


Denna metod tar bort skyddet från dokumentet även om det har ett skyddslösenord.

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Unprotect(const System::String\&) method


Tar bort skyddet från dokumentet om ett korrekt lösenord anges.

```cpp
bool Aspose::Words::Document::Unprotect(const System::String &password)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| password | const System::String\& | Lösenordet för att avskydda dokumentet. |

### ReturnValue

**true** if a correct password was specified and the document was unprotected.
## Anmärkningar


Denna metod avskyddar dokumentet endast om ett korrekt lösenord anges.

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
