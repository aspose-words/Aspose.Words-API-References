---
title: Document.Protect
linktitle: Protect
articleTitle: Protect
second_title: Aspose.Words för .NET
description: Skydda dina dokument enkelt med Document Protect. Förhindra obehöriga ändringar samtidigt som du behåller ditt befintliga lösenord intakt eller använder ett slumpmässigt lösenord.
type: docs
weight: 690
url: /sv/net/aspose.words/document/protect/
---
## Protect(*[ProtectionType](../../protectiontype/)*) {#protect}

Skyddar dokumentet från ändringar utan att ändra det befintliga lösenordet eller tilldelar ett slumpmässigt lösenord.

```csharp
public void Protect(ProtectionType type)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| type | ProtectionType | Anger skyddstypen för dokumentet. |

## Anmärkningar

När ett dokument är skyddat kan användaren endast göra begränsade ändringar, som att lägga till anteckningar, göra ändringar eller fylla i ett formulär.

När du skyddar ett dokument, och dokumentet redan har ett lösenord, ändras inte det befintliga lösenordet.

När du skyddar ett dokument och dokumentet inte har ett lösenord, tilldelar den här metoden ett slumpmässigt lösenord som gör det omöjligt att avskydda dokumentet i Microsoft Word, men du kan fortfarande avskydda dokumentet i Aspose.Words eftersom det inte kräver ett lösenord när skyddet avaktiveras.

## Exempel

Visar hur man stänger av skyddet för en sektion.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Section 1. Hello world!");
builder.InsertBreak(BreakType.SectionBreakNewPage);

builder.Writeln("Section 2. Hello again!");
builder.Write("Please enter text here: ");
builder.InsertTextInput("TextInput1", TextFormFieldType.Regular, "", "Placeholder text", 0);

// Tillämpa skrivskydd på varje avsnitt i dokumentet.
doc.Protect(ProtectionType.AllowOnlyFormFields);

// Stäng av skrivskyddet för den första sektionen.
doc.Sections[0].ProtectedForForms = false;

// I detta utdatadokument kommer vi att kunna redigera det första avsnittet fritt,
// och vi kommer bara att kunna redigera innehållet i formulärfältet i den andra sektionen.
doc.Save(ArtifactsDir + "Section.Protect.docx");
```

### Se även

* enum [ProtectionType](../../protectiontype/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## Protect(*[ProtectionType](../../protectiontype/), string*) {#protect_1}

Skyddar dokumentet från ändringar och ställer in ett lösenord om så önskas.

```csharp
public void Protect(ProtectionType type, string password)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| type | ProtectionType | Anger skyddstypen för dokumentet. |
| password | String | Lösenordet som dokumentet ska skyddas med. Ange`null` eller en tom sträng om du vill skydda dokumentet utan lösenord. |

## Anmärkningar

När ett dokument är skyddat kan användaren endast göra begränsade ändringar, som att lägga till anteckningar, göra ändringar eller fylla i ett formulär.

Observera att dokumentskydd skiljer sig från skrivskydd. Skrivskydd anges med hjälp av[`WriteProtection`](../writeprotection/).

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
