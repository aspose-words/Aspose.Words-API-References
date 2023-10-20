---
title: DocumentBase.ImportNode
linktitle: ImportNode
articleTitle: ImportNode
second_title: Aspose.Words för .NET
description: DocumentBase ImportNode metod. Importerar en nod från ett annat dokument till det aktuella dokumentet i C#.
type: docs
weight: 100
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
| isImportChildren | Boolean | `Sann` att importera alla underordnade noder rekursivt; annat,`falsk`. |

### Returvärde

Den klonade noden som tillhör det aktuella dokumentet.

## Anmärkningar

Denna metod använderUseDestinationStyles alternativ för att lösa formatering.

Genom att importera en nod skapas en kopia av källnoden som tillhör det importerande dokumentet. Den returnerade noden har ingen förälder. Källnoden ändras eller tas inte bort från originaldokumentet.

Innan en nod från ett annat dokument kan infogas i detta dokument måste den importeras. Under import översätts dokumentspecifika egenskaper såsom referenser till stilar och listor från originalet till det importerande dokumentet. Efter att noden har importerats kan den infogas på lämplig plats i dokumentet med[`InsertBefore`](../../compositenode/insertbefore/) eller [`InsertAfter`](../../compositenode/insertafter/).

Om källnoden redan tillhör måldokumentet skapas helt enkelt en djup klon av källnoden.

## Exempel

Visar hur man importerar en nod från ett dokument till ett annat.

```csharp
Document srcDoc = new Document();
Document dstDoc = new Document();

srcDoc.FirstSection.Body.FirstParagraph.AppendChild(
    new Run(srcDoc, "Source document first paragraph text."));
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(
    new Run(dstDoc, "Destination document first paragraph text."));

// Varje nod har ett överordnat dokument, vilket är dokumentet som innehåller noden.
// Att infoga en nod i ett dokument som noden inte tillhör kommer att skapa ett undantag.
Assert.AreNotEqual(dstDoc, srcDoc.FirstSection.Document);
Assert.Throws<ArgumentException>(() => { dstDoc.AppendChild(srcDoc.FirstSection); });

// Använd ImportNode-metoden för att skapa en kopia av en nod, som kommer att ha dokumentet
// som anropade ImportNode-metoden som dess nya ägardokument.
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
| isImportChildren | Boolean | `Sann` att importera alla underordnade noder rekursivt; annat,`falsk`. |
| importFormatMode | ImportFormatMode | Anger hur stilformatering som krockar sammanfogas. |

### Returvärde

Den klonade, importerade noden. Noden tillhör måldokumentet, men har ingen förälder.

## Anmärkningar

Denna överbelastning är användbar för att styra hur stilar och listformatering importeras.

Genom att importera en nod skapas en kopia av källnoden som tillhör det importerande dokumentet. Den returnerade noden har ingen förälder. Källnoden ändras eller tas inte bort från originaldokumentet.

Innan en nod från ett annat dokument kan infogas i detta dokument måste den importeras. Under import översätts dokumentspecifika egenskaper såsom referenser till stilar och listor från originalet till det importerande dokumentet. Efter att noden har importerats kan den infogas på lämplig plats i dokumentet med[`InsertBefore`](../../compositenode/insertbefore/) eller [`InsertAfter`](../../compositenode/insertafter/).

Om källnoden redan tillhör måldokumentet skapas helt enkelt en djup klon av källnoden.

## Exempel

Visar hur man importerar nod från källdokument till måldokument med specifika alternativ.

```csharp
// Skapa två dokument och lägg till en teckenstil till varje dokument.
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

// Importera avsnittet från måldokumentet till källdokumentet, vilket orsakar en stilnamnskollision.
// Om vi använder målstilar kommer den importerade källtexten med samma stilnamn
// som måltext kommer att anta målstilen.
Section importedSection = (Section)dstDoc.ImportNode(srcDoc.FirstSection, true, ImportFormatMode.UseDestinationStyles);
Assert.AreEqual(dstStyle.Font.Name, importedSection.Body.FirstParagraph.Runs[0].Font.Name);
Assert.AreEqual(dstStyle.Name, importedSection.Body.FirstParagraph.Runs[0].Font.StyleName);

// Om vi använder ImportFormatMode.KeepDifferentStyles bevaras källformatet,
// och namnkrocken löser sig genom att lägga till ett suffix.
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
