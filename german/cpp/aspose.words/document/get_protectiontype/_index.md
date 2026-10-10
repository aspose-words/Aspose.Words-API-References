---
title: "Aspose::Words::Document::get_ProtectionType Methode"
linktitle: "get_ProtectionType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::get_ProtectionType Methode. Gibt den aktuell aktiven Dokumentschutztyp in C++ zurück."
type: docs
weight: 44000
url: /de/cpp/aspose.words/document/get_protectiontype/
---
## Document::get_ProtectionType method


Liest den aktuell aktiven Dokumentenschutztyp.

```cpp
Aspose::Words::ProtectionType Aspose::Words::Document::get_ProtectionType()
```

## Hinweise


Diese Eigenschaft ermöglicht das Abrufen des aktuell festgelegten Dokumentschutztyps. Um den Dokumentschutztyp zu ändern, verwenden Sie die Methoden [Protect()](../) und [Unprotect](../unprotect/).

Wenn ein Dokument geschützt ist, kann der Benutzer nur eingeschränkte Änderungen vornehmen, z. B. Anmerkungen hinzufügen, Revisionen erstellen oder ein Formular ausfüllen.

Beachten Sie, dass Dokumentenschutz sich von Schreibschutz unterscheidet. Schreibschutz wird über [WriteProtection](../get_writeprotection/) festgelegt.

## Beispiele



Zeigt, wie man ein Dokument schützt und den Schutz aufhebt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
doc->Protect(Aspose::Words::ProtectionType::ReadOnly, u"password");

ASSERT_EQ(Aspose::Words::ProtectionType::ReadOnly, doc->get_ProtectionType());

// Wenn wir dieses Dokument mit Microsoft Word öffnen, um es zu bearbeiten,
// müssen wir das Passwort eingeben, um die Schutzvorrichtung zu überwinden.
doc->Save(get_ArtifactsDir() + u"Document.Protect.docx");

// Beachten Sie, dass der Schutz nur für Microsoft Word‑Benutzer gilt, die unser Dokument öffnen.
// Wir haben das Dokument in keiner Weise verschlüsselt, und wir benötigen das Passwort nicht, um es programmgesteuert zu öffnen und zu bearbeiten.
auto protectedDoc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.Protect.docx");

ASSERT_EQ(Aspose::Words::ProtectionType::ReadOnly, protectedDoc->get_ProtectionType());

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(protectedDoc);
builder->Writeln(u"Text added to a protected document.");

// Es gibt zwei Möglichkeiten, den Schutz eines Dokuments zu entfernen.
// 1 - Ohne Passwort:
doc->Unprotect();

ASSERT_EQ(Aspose::Words::ProtectionType::NoProtection, doc->get_ProtectionType());

doc->Protect(Aspose::Words::ProtectionType::ReadOnly, u"NewPassword");

ASSERT_EQ(Aspose::Words::ProtectionType::ReadOnly, doc->get_ProtectionType());

doc->Unprotect(u"WrongPassword");

ASSERT_EQ(Aspose::Words::ProtectionType::ReadOnly, doc->get_ProtectionType());

// 2 - Mit dem korrekten Passwort:
doc->Unprotect(u"NewPassword");

ASSERT_EQ(Aspose::Words::ProtectionType::NoProtection, doc->get_ProtectionType());
```

## Siehe auch

* Enum [ProtectionType](../../protectiontype/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
