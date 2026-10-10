---
title: "Aspose::Words::Properties::DocumentSecurity enum"
linktitle: "DocumentSecurity"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Properties::DocumentSecurity enum. Wird als Wert für die Security‑Eigenschaft verwendet. Gibt die Sicherheitsstufe eines Dokuments als numerischen Wert in C++ an."
type: docs
weight: 5000
url: /de/cpp/aspose.words.properties/documentsecurity/
---
## DocumentSecurity enum


Wird als Wert für die [Security](../builtindocumentproperties/get_security/)‑Eigenschaft verwendet. Gibt die Sicherheitsstufe eines Dokuments als numerischen Wert an.

```cpp
enum class DocumentSecurity
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Keine | 0 | Für die Eigenschaft sind keine Sicherheitszustände angegeben. |
| PasswordProtected | 1 | Das Dokument ist passwortgeschützt. (Hinweis: Dies wurde bisher in keinem Dokument gesehen). |
| ReadOnlyRecommended | 2 | Das Dokument soll, wenn möglich, schreibgeschützt geöffnet werden, aber die Einstellung kann überschrieben werden. |
| ReadOnlyEnforced | 4 | Das Dokument wird immer schreibgeschützt geöffnet. |
| ReadOnlyExceptAnnotations | 8 | Das Dokument wird immer schreibgeschützt geöffnet, außer für Anmerkungen. |


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

* Namespace [Aspose::Words::Properties](../)
* Library [Aspose.Words for C++](../../)
