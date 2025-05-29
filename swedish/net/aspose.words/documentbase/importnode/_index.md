---
title: DocumentBase.ImportNode
linktitle: ImportNode
articleTitle: ImportNode
second_title: Aspose.Words för .NET
description: Importera enkelt noder från andra dokument för att förbättra ditt arbetsflöde med DocumentBases ImportNode-metod. Effektivisera din dokumenthantering idag!
type: docs
weight: 110
url: /sv/net/aspose.words/documentbase/importnode/
---
## ImportNode(*[Node](../../node/), bool*) {#importnode}

Importerar en nod från ett annat dokument till det aktuella dokumentet.

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| srcNode | Node | Noden som importeras. |
| isImportChildren | Boolean | `sann` att importera alla underordnade noder rekursivt; annars,`falsk`. |

### Returvärde

Den klonade noden som tillhör det aktuella dokumentet.

## Anmärkningar

Den här metoden använderUseDestinationStyles alternativ för att lösa formatering.

Import av en nod skapar en kopia av källnoden som tillhör det importerande dokumentet. Den returnerade noden har ingen förälder. Källnoden ändras eller tas inte bort från originaldokumentet.

Innan en nod från ett annat dokument kan infogas i detta dokument måste den importeras. Under importen översätts dokumentspecifika egenskaper, såsom referenser till format och listor, från originalet till det importerande dokumentet. Efter att noden har importerats kan den infogas på lämplig plats i dokumentet med hjälp av[`InsertBefore`](../../compositenode/insertbefore/) eller [`InsertAfter`](../../compositenode/insertafter/).

Om källnoden redan tillhör destinationsdokumentet skapas helt enkelt en djup clone av källnoden.

## Exempel

Visar hur man importerar en nod från ett dokument till ett annat.

```csharp
Document srcDoc = new Document();
Document dstDoc = new Document();

srcDoc.FirstSection.Body.FirstParagraph.AppendChild(
    new Run(srcDoc, "Source document first paragraph text."));
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(
    new Run(dstDoc, "Destination document first paragraph text."));

// Varje nod har ett föräldradokument, vilket är det dokument som innehåller noden.
// Att infoga en nod i ett dokument som noden inte tillhör kommer att utlösa ett undantag.
Assert.AreNotEqual(dstDoc, srcDoc.FirstSection.Document);
Assert.Throws<ArgumentException>(() => dstDoc.AppendChild(srcDoc.FirstSection));

// Använd ImportNode-metoden för att skapa en kopia av en nod, som kommer att innehålla dokumentet
// som anropade ImportNode-metoden och sattes som sitt nya ägardokument.
Section importedSection = (Section)dstDoc.ImportNode(srcDoc.FirstSection, true);

Assert.AreEqual(dstDoc, importedSection.Document);

// Vi kan nu infoga noden i dokumentet.
dstDoc.AppendChild(importedSection);

Assert.AreEqual("Destination document first paragraph text.\r\nSource document first paragraph text.\r\n",
    dstDoc.ToString(SaveFormat.Text));
```

### Se även

* class [Node](../../node/)
* class [DocumentBase](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## ImportNode(*[Node](../../node/), bool, [ImportFormatMode](../../importformatmode/)*) {#importnode_1}

Importerar en nod från ett annat dokument till det aktuella dokumentet med ett alternativ för att styra formateringen.

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren, ImportFormatMode importFormatMode)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| srcNode | Node | Noden som ska importeras. |
| isImportChildren | Boolean | `sann` att importera alla underordnade noder rekursivt; annars,`falsk`. |
| importFormatMode | ImportFormatMode | Anger hur formatering som krockar ska sammanfogas. |

### Returvärde

Den klonade, importerade noden. Noden tillhör destinationsdokumentet, men har ingen överordnad nod.

## Anmärkningar

Denna överbelastning är användbar för att styra hur stilar och listformatering importeras.

Import av en nod skapar en kopia av källnoden som tillhör det importerande dokumentet. Den returnerade noden har ingen förälder. Källnoden ändras eller tas inte bort från originaldokumentet.

Innan en nod från ett annat dokument kan infogas i detta dokument måste den importeras. Under importen översätts dokumentspecifika egenskaper, såsom referenser till format och listor, från originalet till det importerande dokumentet. Efter att noden har importerats kan den infogas på lämplig plats i dokumentet med hjälp av[`InsertBefore`](../../compositenode/insertbefore/) eller [`InsertAfter`](../../compositenode/insertafter/).

Om källnoden redan tillhör destinationsdokumentet skapas helt enkelt en djup clone av källnoden.

## Exempel

Visar hur man importerar en nod från ett källdokument till ett destinationsdokument med specifika alternativ.

```csharp
// Skapa två dokument och lägg till ett teckenformat i varje dokument.
// Konfigurera stilarna så att de har samma namn, men olika textformatering.
Document srcDoc = new Document();
Style srcStyle = srcDoc.Styles.Add(StyleType.Character, "My style");
srcStyle.Font.Name = "Courier New";
DocumentBuilder srcBuilder = new DocumentBuilder(srcDoc);
srcBuilder.Font.Style = srcStyle;
srcBuilder.Writeln("Source document text.");

Document dstDoc = new Document();
Style dstStyle = dstDoc.Styles.Add(StyleType.Character, "My style");
dstStyle.Font.Name = "Calibri";
DocumentBuilder dstBuilder = new DocumentBuilder(dstDoc);
dstBuilder.Font.Style = dstStyle;
dstBuilder.Writeln("Destination document text.");

// Importera avsnittet från destinationsdokumentet till källdokumentet, vilket orsakar en stilnamnskollision.
// Om vi använder destinationsstilar, då importeras källtexten med samma stilnamn
// som destinationstext kommer att anta destinationsstilen.
Section importedSection = (Section)dstDoc.ImportNode(srcDoc.FirstSection, true, ImportFormatMode.UseDestinationStyles);
Assert.AreEqual(dstStyle.Font.Name, importedSection.Body.FirstParagraph.Runs[0].Font.Name);
Assert.AreEqual(dstStyle.Name, importedSection.Body.FirstParagraph.Runs[0].Font.StyleName);

// Om vi använder ImportFormatMode.KeepDifferentStyles, bevaras källstilen,
// och namnkonflikten löses genom att lägga till ett suffix.
dstDoc.ImportNode(srcDoc.FirstSection, true, ImportFormatMode.KeepDifferentStyles);
Assert.AreEqual(dstStyle.Font.Name, dstDoc.Styles["My style"].Font.Name);
Assert.AreEqual(srcStyle.Font.Name, dstDoc.Styles["My style_0"].Font.Name);
```

### Se även

* class [Node](../../node/)
* enum [ImportFormatMode](../../importformatmode/)
* class [DocumentBase](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
