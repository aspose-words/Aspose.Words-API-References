---
title: DocumentSecurity Enum
linktitle: DocumentSecurity
articleTitle: DocumentSecurity
second_title: Aspose.Words für .NET
description: Entdecken Sie die Enumeration Aspose.Words.DocumentSecurity, um die Sicherheit Ihres Dokuments zu verbessern. Definieren und verwalten Sie Sicherheitsstufen für optimalen Schutz ganz einfach.
type: docs
weight: 5220
url: /de/net/aspose.words.properties/documentsecurity/
---
## DocumentSecurity enumeration

Wird als Wert für die[`Security`](../builtindocumentproperties/security/) property. Gibt die Sicherheitsstufe eines Dokuments als numerischen Wert an.

```csharp
[Flags]
public enum DocumentSecurity
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Die Eigenschaft gibt keine Sicherheitszustände an. |
| PasswordProtected | `1` | Das Dokument ist passwortgeschützt. (Hinweis wurde bisher noch nie in einem Dokument gesehen). |
| ReadOnlyRecommended | `2` | Das Dokument soll nach Möglichkeit schreibgeschützt geöffnet werden, die Einstellung kann jedoch überschrieben werden. |
| ReadOnlyEnforced | `4` | Das Dokument soll immer schreibgeschützt geöffnet werden. |
| ReadOnlyExceptAnnotations | `8` | Das Dokument soll immer schreibgeschützt geöffnet werden, außer für Anmerkungen. |

## Beispiele

Zeigt, wie Sie Dokumenteigenschaften verwenden, um die Sicherheitsstufe eines Dokuments anzuzeigen.

```csharp
Document doc = new Document();

Assert.AreEqual(DocumentSecurity.None, doc.BuiltInDocumentProperties.Security);

// Wenn wir ein Dokument als schreibgeschützt konfigurieren, wird dieser Status mithilfe der integrierten Eigenschaft „Sicherheit“ angezeigt.
doc.WriteProtection.ReadOnlyRecommended = true;
doc.Save(ArtifactsDir + "DocumentProperties.Security.ReadOnlyRecommended.docx");

Assert.AreEqual(DocumentSecurity.ReadOnlyRecommended, 
    new Document(ArtifactsDir + "DocumentProperties.Security.ReadOnlyRecommended.docx").BuiltInDocumentProperties.Security);

// Schützen Sie ein Dokument mit einem Schreibschutz und überprüfen Sie dann seine Sicherheitsstufe.
doc = new Document();

Assert.False(doc.WriteProtection.IsWriteProtected);

doc.WriteProtection.SetPassword("MyPassword");

Assert.True(doc.WriteProtection.ValidatePassword("MyPassword"));
Assert.True(doc.WriteProtection.IsWriteProtected);

doc.Save(ArtifactsDir + "DocumentProperties.Security.ReadOnlyEnforced.docx");

Assert.AreEqual(DocumentSecurity.ReadOnlyEnforced,
    new Document(ArtifactsDir + "DocumentProperties.Security.ReadOnlyEnforced.docx").BuiltInDocumentProperties.Security);

// „Sicherheit“ ist eine beschreibende Eigenschaft. Wir können ihren Wert manuell bearbeiten.
doc = new Document();

doc.Protect(ProtectionType.AllowOnlyComments, "MyPassword");
doc.BuiltInDocumentProperties.Security = DocumentSecurity.ReadOnlyExceptAnnotations;
doc.Save(ArtifactsDir + "DocumentProperties.Security.ReadOnlyExceptAnnotations.docx");

Assert.AreEqual(DocumentSecurity.ReadOnlyExceptAnnotations,
    new Document(ArtifactsDir + "DocumentProperties.Security.ReadOnlyExceptAnnotations.docx").BuiltInDocumentProperties.Security);
```

### Siehe auch

* namensraum [Aspose.Words.Properties](../../aspose.words.properties/)
* Montage [Aspose.Words](../../)
