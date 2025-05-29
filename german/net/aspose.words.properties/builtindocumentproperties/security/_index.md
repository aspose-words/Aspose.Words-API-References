---
title: BuiltInDocumentProperties.Security
linktitle: Security
articleTitle: Security
second_title: Aspose.Words für .NET
description: Entdecken Sie die Sicherheitsfunktion „BuiltInDocumentProperties“, die die Sicherheitsstufe Ihres Dokuments präzise definiert. Verbessern Sie noch heute Ihren Dokumentenschutz!
type: docs
weight: 270
url: /de/net/aspose.words.properties/builtindocumentproperties/security/
---
## BuiltInDocumentProperties.Security property

Gibt die Sicherheitsstufe eines Dokuments als numerischen Wert an.

```csharp
public DocumentSecurity Security { get; set; }
```

## Bemerkungen

Verwenden Sie diese Eigenschaft nur zu Informationszwecken, da sie in Microsoft Word nicht immer festgelegt wird. Diese Eigenschaft ist nur in DOC- und OOXML-Dokumenten verfügbar.

Um ein Dokument zu schützen oder den Schutz aufzuheben, verwenden Sie die Funktion [`Protect`](../../../aspose.words/document/protect/) Und[`Unprotect`](../../../aspose.words/document/unprotect/) Methoden.

Aspose.Words aktualisiert diese Eigenschaft vor dem Speichern eines Dokuments auf einen korrekten Wert.

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

* enum [DocumentSecurity](../../documentsecurity/)
* class [BuiltInDocumentProperties](../)
* namensraum [Aspose.Words.Properties](../../../aspose.words.properties/)
* Montage [Aspose.Words](../../../)
