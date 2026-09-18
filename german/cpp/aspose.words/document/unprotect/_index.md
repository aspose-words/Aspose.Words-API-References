---
title: "Aspose::Words::Document::Unprotect Methode"
linktitle: "Unprotect"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::Unprotect Methode. Entfernt den Schutz des Dokuments unabhängig vom Passwort in C++."
type: docs
weight: 95000
url: /de/cpp/aspose.words/document/unprotect/
---
## Document::Unprotect() method


Entfernt den Schutz des Dokuments, unabhängig vom Passwort.

```cpp
void Aspose::Words::Document::Unprotect()
```

## Hinweise


Diese Methode hebt den Schutz des Dokuments auf, selbst wenn ein Schutzpasswort vorhanden ist.

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Unprotect(const System::String\&) method


Entfernt den Schutz des Dokuments, wenn ein korrektes Passwort angegeben wird.

```cpp
bool Aspose::Words::Document::Unprotect(const System::String &password)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| password | const System::String\& | Das Passwort, mit dem der Dokumentenschutz aufgehoben wird. |

### ReturnValue

**true** if a correct password was specified and the document was unprotected.
## Hinweise


Diese Methode hebt den Dokumentenschutz nur auf, wenn ein korrektes Passwort angegeben wird.

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
