---
title: Enum DocumentSecurity
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Properties.DocumentSecurity opsomming. Wird als Wert für verwendetSecurity property. Gibt die Sicherheitsstufe eines Dokuments als numerischen Wert an.
type: docs
weight: 4490
url: /de/net/aspose.words.properties/documentsecurity/
---
## DocumentSecurity enumeration

Wird als Wert für verwendet[`Security`](../builtindocumentproperties/security/) property. Gibt die Sicherheitsstufe eines Dokuments als numerischen Wert an.

```csharp
[Flags]
public enum DocumentSecurity
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Es sind keine durch die Eigenschaft angegebenen Sicherheitszustände vorhanden. |
| PasswordProtected | `1` | Das Dokument ist passwortgeschützt. (Hinweis wurde bisher noch nie in einem Dokument gesehen). |
| ReadOnlyRecommended | `2` | Das Dokument soll nach Möglichkeit schreibgeschützt geöffnet werden, die Einstellung kann jedoch überschrieben werden. |
| ReadOnlyEnforced | `4` | Das Dokument, das immer schreibgeschützt geöffnet werden soll. |
| ReadOnlyExceptAnnotations | `8` | Das Dokument soll immer schreibgeschützt geöffnet werden, mit Ausnahme von Anmerkungen. |

### Beispiele

Zeigt, wie Dokumenteigenschaften verwendet werden, um die Sicherheitsstufe eines Dokuments anzuzeigen.

```csharp
Document doc = new Document();

Assert.AreEqual(DocumentSecurity.None, doc.BuiltInDocumentProperties.Security);

// Wenn wir ein Dokument als schreibgeschützt konfigurieren, zeigt es diesen Status mithilfe der integrierten Eigenschaft „Sicherheit“ an.
doc.WriteProtection.ReadOnlyRecommended = true;
doc.Save(ArtifactsDir + "DocumentProperties.Security.ReadOnlyRecommended.docx");

Assert.AreEqual(DocumentSecurity.ReadOnlyRecommended, 
    new Document(ArtifactsDir + "DocumentProperties.Security.ReadOnlyRecommended.docx").BuiltInDocumentProperties.Security);

// Schreibschützen Sie ein Dokument und überprüfen Sie dann seine Sicherheitsstufe.
doc = new Document();

Assert.False(doc.WriteProtection.IsWriteProtected);

doc.WriteProtection.SetPassword("MyPassword");

Assert.True(doc.WriteProtection.ValidatePassword("MyPassword"));
Assert.True(doc.WriteProtection.IsWriteProtected);

doc.Save(ArtifactsDir + "DocumentProperties.Security.ReadOnlyEnforced.docx");

Assert.AreEqual(DocumentSecurity.ReadOnlyEnforced,
    new Document(ArtifactsDir + "DocumentProperties.Security.ReadOnlyEnforced.docx").BuiltInDocumentProperties.Security);

// „Sicherheit“ ist eine beschreibende Eigenschaft. Wir können seinen Wert manuell bearbeiten.
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


