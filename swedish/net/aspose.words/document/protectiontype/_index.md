---
title: Document.ProtectionType
linktitle: ProtectionType
articleTitle: ProtectionType
second_title: Aspose.Words för .NET
description: Upptäck den aktiva dokumentskyddstypen för förbättrad säkerhet och dataintegritet. Skydda dina filer enkelt med våra avancerade funktioner.
type: docs
weight: 340
url: /sv/net/aspose.words/document/protectiontype/
---
## Document.ProtectionType property

Hämtar den aktiva dokumentskyddstypen.

```csharp
public ProtectionType ProtectionType { get; }
```

## Anmärkningar

Den här egenskapen gör det möjligt att hämta den aktuellt inställda dokumentskyddstypen. För att ändra dokumentskyddstypen, använd[`Protect`](../protect/) och[`Unprotect`](../unprotect/) metoder.

När ett dokument är skyddat kan användaren endast göra begränsade ändringar, som att lägga till anteckningar, göra ändringar eller fylla i ett formulär.

Observera att dokumentskydd skiljer sig från skrivskydd. Skrivskydd anges med hjälp av[`WriteProtection`](../writeprotection/)

## Exempel

Visar hur man skyddar och avskyddar ett dokument.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "password");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// Om vi öppnar det här dokumentet med Microsoft Word och avser att redigera det,
// vi måste ange lösenordet för att komma igenom skyddet.
doc.Save(ArtifactsDir + "Document.Protect.docx");

// Observera att skyddet endast gäller Microsoft Word-användare som öppnar vårt dokument.
// Vi har inte krypterat dokumentet på något sätt, och vi behöver inte lösenordet för att öppna och redigera det programmatiskt.
Document protectedDoc = new Document(ArtifactsDir + "Document.Protect.docx");

Assert.AreEqual(ProtectionType.ReadOnly, protectedDoc.ProtectionType);

DocumentBuilder builder = new DocumentBuilder(protectedDoc);
builder.Writeln("Text added to a protected document.");
// Det finns två sätt att ta bort skyddet från ett dokument.
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

* enum [ProtectionType](../../protectiontype/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
