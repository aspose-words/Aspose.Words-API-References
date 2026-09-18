---
title: "Aspose::Words::Document::Protect Methode"
linktitle: "Protect"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::Protect Methode. Schützt das Dokument vor Änderungen, ohne das vorhandene Passwort zu ändern, oder weist ein zufälliges Passwort zu in C++."
type: docs
weight: 67000
url: /de/cpp/aspose.words/document/protect/
---
## Document::Protect(Aspose::Words::ProtectionType) method


Schützt das Dokument vor Änderungen, ohne das vorhandene Passwort zu ändern, oder weist ein zufälliges Passwort zu.

```cpp
void Aspose::Words::Document::Protect(Aspose::Words::ProtectionType type)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Typ | Aspose::Words::ProtectionType | Gibt den Schutztyp für das Dokument an. |
## Hinweise


Wenn ein Dokument geschützt ist, kann der Benutzer nur eingeschränkte Änderungen vornehmen, z. B. Anmerkungen hinzufügen, Revisionen erstellen oder ein Formular ausfüllen.

Wenn Sie ein Dokument schützen und das Dokument bereits ein Schutzpasswort hat, wird das vorhandene Schutzpasswort nicht geändert.

Wenn Sie ein Dokument schützen und das Dokument kein Schutzpasswort hat, weist diese Methode ein zufälliges Passwort zu, das es unmöglich macht, das Dokument in Microsoft Word zu entsperren, Sie können das Dokument jedoch weiterhin in Aspose.Words entsperren, da beim Entschlüsseln kein Passwort erforderlich ist.

## Beispiele



Zeigt, wie man den Schutz für einen Abschnitt deaktiviert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Section 1. Hello world!");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

builder->Writeln(u"Section 2. Hello again!");
builder->Write(u"Please enter text here: ");
builder->InsertTextInput(u"TextInput1", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Placeholder text", 0);

// Wenden Sie Schreibschutz auf jeden Abschnitt im Dokument an.
doc->Protect(Aspose::Words::ProtectionType::AllowOnlyFormFields);

// Deaktivieren Sie den Schreibschutz für den ersten Abschnitt.
doc->get_Sections()->idx_get(0)->set_ProtectedForForms(false);

// In diesem Ausgabedokument können wir den ersten Abschnitt frei bearbeiten,
// und wir können nur den Inhalt des Formularfelds im zweiten Abschnitt bearbeiten.
doc->Save(get_ArtifactsDir() + u"Section.Protect.docx");
```

## Siehe auch

* Enum [ProtectionType](../../protectiontype/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Protect(Aspose::Words::ProtectionType, const System::String\&) method


Schützt das Dokument vor Änderungen und legt optional ein Schutzpasswort fest.

```cpp
void Aspose::Words::Document::Protect(Aspose::Words::ProtectionType type, const System::String &password)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Typ | Aspose::Words::ProtectionType | Gibt den Schutztyp für das Dokument an. |
| password | const System::String\& | Das Passwort, mit dem das Dokument geschützt werden soll. Geben Sie **null** oder einen leeren String an, wenn Sie das Dokument ohne Passwort schützen möchten. |
## Hinweise


Wenn ein Dokument geschützt ist, kann der Benutzer nur eingeschränkte Änderungen vornehmen, z. B. Anmerkungen hinzufügen, Revisionen erstellen oder ein Formular ausfüllen.

Beachten Sie, dass der Dokumentenschutz sich vom Schreibschutz unterscheidet. Schreibschutz wird über die [WriteProtection](../get_writeprotection/) angegeben.

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
