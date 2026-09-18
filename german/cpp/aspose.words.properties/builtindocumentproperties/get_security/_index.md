---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Security Methode"
linktitle: "get_Security"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Security Methode. Gibt das Sicherheitsniveau eines Dokuments als numerischen Wert in C++ an."
type: docs
weight: 25000
url: /de/cpp/aspose.words.properties/builtindocumentproperties/get_security/
---
## BuiltInDocumentProperties::get_Security method


Gibt das Sicherheitsniveau eines Dokuments als numerischen Wert an.

```cpp
Aspose::Words::Properties::DocumentSecurity Aspose::Words::Properties::BuiltInDocumentProperties::get_Security()
```

## Hinweise


Verwenden Sie diese Eigenschaft nur zu Informationszwecken, da Microsoft Word diese Eigenschaft nicht immer setzt. Diese Eigenschaft ist nur in DOC- und OOXML-Dokumenten verfügbar.

Um ein Dokument zu schützen oder den Schutz aufzuheben, verwenden Sie die Methoden [Protect()](../) und [Unprotect](../../../aspose.words/document/unprotect/).

Aspose.Words aktualisiert diese Eigenschaft vor dem Speichern eines Dokuments auf einen korrekten Wert.

## Beispiele



Zeigt, wie Dokumenteigenschaften verwendet werden, um die Sicherheitsstufe eines Dokuments anzuzeigen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_EQ(Aspose::Words::Properties::DocumentSecurity::None, doc->get_BuiltInDocumentProperties()->get_Security());

// Wenn wir ein Dokument schreibgeschützt konfigurieren, wird dieser Status über die integrierte Eigenschaft \"Security\" angezeigt.
doc->get_WriteProtection()->set_ReadOnlyRecommended(true);
doc->Save(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyRecommended.docx");

ASSERT_EQ(Aspose::Words::Properties::DocumentSecurity::ReadOnlyRecommended, System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyRecommended.docx")->get_BuiltInDocumentProperties()->get_Security());

// Schreibschutz für ein Dokument aktivieren und anschließend die Sicherheitsstufe überprüfen.
doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_FALSE(doc->get_WriteProtection()->get_IsWriteProtected());

doc->get_WriteProtection()->SetPassword(u"MyPassword");

ASSERT_TRUE(doc->get_WriteProtection()->ValidatePassword(u"MyPassword"));
ASSERT_TRUE(doc->get_WriteProtection()->get_IsWriteProtected());

doc->Save(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyEnforced.docx");

ASSERT_EQ(Aspose::Words::Properties::DocumentSecurity::ReadOnlyEnforced, System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyEnforced.docx")->get_BuiltInDocumentProperties()->get_Security());

// \"Security\" ist eine beschreibende Eigenschaft. Wir können ihren Wert manuell bearbeiten.
doc = System::MakeObject<Aspose::Words::Document>();

doc->Protect(Aspose::Words::ProtectionType::AllowOnlyComments, u"MyPassword");
doc->get_BuiltInDocumentProperties()->set_Security(Aspose::Words::Properties::DocumentSecurity::ReadOnlyExceptAnnotations);
doc->Save(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyExceptAnnotations.docx");

ASSERT_EQ(Aspose::Words::Properties::DocumentSecurity::ReadOnlyExceptAnnotations, System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocumentProperties.Security.ReadOnlyExceptAnnotations.docx")->get_BuiltInDocumentProperties()->get_Security());
```

## Siehe auch

* Enum [DocumentSecurity](../../documentsecurity/)
* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
