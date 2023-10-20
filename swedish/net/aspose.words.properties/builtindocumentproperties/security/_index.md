---
title: BuiltInDocumentProperties.Security
linktitle: Security
articleTitle: Security
second_title: Aspose.Words för .NET
description: BuiltInDocumentProperties Security fast egendom. Anger säkerhetsnivån för ett dokument som ett numeriskt värde i C#.
type: docs
weight: 250
url: /sv/net/aspose.words.properties/builtindocumentproperties/security/
---
## BuiltInDocumentProperties.Security property

Anger säkerhetsnivån för ett dokument som ett numeriskt värde.

```csharp
public DocumentSecurity Security { get; set; }
```

## Anmärkningar

Använd den här egenskapen endast i informationssyfte eftersom Microsoft Word inte alltid anger den här egenskapen. Den här egenskapen är endast tillgänglig i DOC- och OOXML-dokument.

För att skydda eller avskydda ett dokument använd the [`Protect`](../../../aspose.words/document/protect/) och[`Unprotect`](../../../aspose.words/document/unprotect/) metoder.

Aspose.Words uppdaterar den här egenskapen till ett korrekt värde innan ett dokument sparas.

## Exempel

Visar hur du använder dokumentegenskaper för att visa säkerhetsnivån för ett dokument.

```csharp
Document doc = new Document();

Assert.AreEqual(DocumentSecurity.None, doc.BuiltInDocumentProperties.Security);

// Om vi konfigurerar ett dokument att vara skrivskyddat kommer det att visa denna status med den inbyggda "Security"-egenskapen.
doc.WriteProtection.ReadOnlyRecommended = true;
doc.Save(ArtifactsDir + "DocumentProperties.Security.ReadOnlyRecommended.docx");

Assert.AreEqual(DocumentSecurity.ReadOnlyRecommended, 
    new Document(ArtifactsDir + "DocumentProperties.Security.ReadOnlyRecommended.docx").BuiltInDocumentProperties.Security);

// Skrivskydda ett dokument och verifiera sedan dess säkerhetsnivå.
doc = new Document();

Assert.False(doc.WriteProtection.IsWriteProtected);

doc.WriteProtection.SetPassword("MyPassword");

Assert.True(doc.WriteProtection.ValidatePassword("MyPassword"));
Assert.True(doc.WriteProtection.IsWriteProtected);

doc.Save(ArtifactsDir + "DocumentProperties.Security.ReadOnlyEnforced.docx");

Assert.AreEqual(DocumentSecurity.ReadOnlyEnforced,
    new Document(ArtifactsDir + "DocumentProperties.Security.ReadOnlyEnforced.docx").BuiltInDocumentProperties.Security);

// "Säkerhet" är en beskrivande egenskap. Vi kan redigera dess värde manuellt.
doc = new Document();

doc.Protect(ProtectionType.AllowOnlyComments, "MyPassword");
doc.BuiltInDocumentProperties.Security = DocumentSecurity.ReadOnlyExceptAnnotations;
doc.Save(ArtifactsDir + "DocumentProperties.Security.ReadOnlyExceptAnnotations.docx");

Assert.AreEqual(DocumentSecurity.ReadOnlyExceptAnnotations,
    new Document(ArtifactsDir + "DocumentProperties.Security.ReadOnlyExceptAnnotations.docx").BuiltInDocumentProperties.Security);
```

### Se även

* enum [DocumentSecurity](../../documentsecurity/)
* class [BuiltInDocumentProperties](../)
* namnutrymme [Aspose.Words.Properties](../../../aspose.words.properties/)
* hopsättning [Aspose.Words](../../../)
