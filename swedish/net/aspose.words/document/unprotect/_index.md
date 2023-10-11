---
title: Document.Unprotect
second_title: Aspose.Words för .NET API Referens
description: Document metod. Tar bort skyddet från dokumentet oavsett lösenord.
type: docs
weight: 760
url: /sv/net/aspose.words/document/unprotect/
---
## Unprotect() {#unprotect_1}

Tar bort skyddet från dokumentet oavsett lösenord.

```csharp
public void Unprotect()
```

### Anmärkningar

Denna metod tar bort skyddet av dokumentet även om det har ett skyddslösenord.

Observera att dokumentskydd skiljer sig från skrivskydd. Skrivskydd specificeras med hjälp av[`WriteProtection`](../writeprotection/).

### Exempel

Visar hur man skyddar och avskyddar ett dokument.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "password");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// Om vi öppnar det här dokumentet med Microsoft Word för att redigera det,
// vi kommer att behöva använda lösenordet för att komma igenom skyddet.
doc.Save(ArtifactsDir + "Document.Protect.docx");

// Observera att skyddet endast gäller för Microsoft Word-användare som öppnar vårt dokument.
// Vi har inte krypterat dokumentet på något sätt, och vi behöver inte lösenordet för att öppna och redigera det programmatiskt.
Document protectedDoc = new Document(ArtifactsDir + "Document.Protect.docx");

Assert.AreEqual(ProtectionType.ReadOnly, protectedDoc.ProtectionType);

DocumentBuilder builder = new DocumentBuilder(protectedDoc);
builder.Writeln("Text added to a protected document.");
// Det finns två sätt att ta bort skydd från ett dokument.
// 1 - Utan lösenord:
doc.Unprotect();

Assert.AreEqual(ProtectionType.NoProtection, doc.ProtectionType);

doc.Protect(ProtectionType.ReadOnly, "NewPassword");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

doc.Unprotect("WrongPassword");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// 2 - Med rätt lösenord:
doc.Unprotect("NewPassword");

Assert.AreEqual(ProtectionType.NoProtection, doc.ProtectionType);
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../document/)
* hopsättning [Aspose.Words](../../../)

---

## Unprotect(string) {#unprotect}

Tar bort skyddet från dokumentet om ett korrekt lösenord anges.

```csharp
public bool Unprotect(string password)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| password | String | Lösenordet att avskydda dokumentet med. |

### Returvärde

`Sann` om ett korrekt lösenord angavs och dokumentet var oskyddat.

### Anmärkningar

Den här metoden tar bara bort dokumentets skydd om ett korrekt lösenord anges.

Observera att dokumentskydd skiljer sig från skrivskydd. Skrivskydd specificeras med hjälp av[`WriteProtection`](../writeprotection/).

### Exempel

Visar hur man skyddar och avskyddar ett dokument.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "password");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// Om vi öppnar det här dokumentet med Microsoft Word för att redigera det,
// vi kommer att behöva använda lösenordet för att komma igenom skyddet.
doc.Save(ArtifactsDir + "Document.Protect.docx");

// Observera att skyddet endast gäller för Microsoft Word-användare som öppnar vårt dokument.
// Vi har inte krypterat dokumentet på något sätt, och vi behöver inte lösenordet för att öppna och redigera det programmatiskt.
Document protectedDoc = new Document(ArtifactsDir + "Document.Protect.docx");

Assert.AreEqual(ProtectionType.ReadOnly, protectedDoc.ProtectionType);

DocumentBuilder builder = new DocumentBuilder(protectedDoc);
builder.Writeln("Text added to a protected document.");
// Det finns två sätt att ta bort skydd från ett dokument.
// 1 - Utan lösenord:
doc.Unprotect();

Assert.AreEqual(ProtectionType.NoProtection, doc.ProtectionType);

doc.Protect(ProtectionType.ReadOnly, "NewPassword");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

doc.Unprotect("WrongPassword");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// 2 - Med rätt lösenord:
doc.Unprotect("NewPassword");

Assert.AreEqual(ProtectionType.NoProtection, doc.ProtectionType);
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../document/)
* hopsättning [Aspose.Words](../../../)


