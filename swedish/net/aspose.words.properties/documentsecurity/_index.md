---
title: DocumentSecurity Enum
linktitle: DocumentSecurity
articleTitle: DocumentSecurity
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.DocumentSecurity-enum för att förbättra säkerheten i ditt dokument. Ange och hantera enkelt säkerhetsnivåer för optimalt skydd.
type: docs
weight: 5220
url: /sv/net/aspose.words.properties/documentsecurity/
---
## DocumentSecurity enumeration

Används som ett värde för[`Security`](../builtindocumentproperties/security/) property. Anger säkerhetsnivån för ett dokument som ett numeriskt värde.

```csharp
[Flags]
public enum DocumentSecurity
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `0` | Inga säkerhetstillstånd har angetts av egenskapen. |
| PasswordProtected | `1` | Dokumentet är lösenordsskyddat. (Anteckningen har aldrig setts i ett dokument hittills). |
| ReadOnlyRecommended | `2` | Dokumentet ska öppnas skrivskyddat om möjligt, men inställningen kan åsidosättas. |
| ReadOnlyEnforced | `4` | Dokumentet som alltid ska öppnas skrivskyddat. |
| ReadOnlyExceptAnnotations | `8` | Dokumentet ska alltid öppnas skrivskyddat förutom för anteckningar. |

## Exempel

Visar hur man använder dokumentegenskaper för att visa ett dokuments säkerhetsnivå.

```csharp
Document doc = new Document();

Assert.AreEqual(DocumentSecurity.None, doc.BuiltInDocumentProperties.Security);

// Om vi konfigurerar ett dokument som skrivskyddat, kommer det att visa denna status med hjälp av den inbyggda egenskapen "Säkerhet".
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

* namnutrymme [Aspose.Words.Properties](../../aspose.words.properties/)
* hopsättning [Aspose.Words](../../)
