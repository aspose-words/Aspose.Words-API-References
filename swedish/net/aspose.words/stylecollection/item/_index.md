---
title: StyleCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words för .NET
description: Upptäck StyleCollections kraftfulla Item-egenskap för att enkelt hämta stilar efter namn eller alias, vilket enkelt förbättrar din designupplevelse!
type: docs
weight: 50
url: /sv/net/aspose.words/stylecollection/item/
---
## StyleCollection indexer (1 of 3)

Hämtar en stil efter namn eller alias.

```csharp
public Style this[string name] { get; }
```

## Anmärkningar

Skiftlägeskänsligt, returer`null` om stilen med det angivna namnet inte hittas.

Om detta är ett engelskt namn på en byggstil som ännu inte finns, skapas det automatiskt.

## Exempel

Visar när dokumentets sidlayout ska beräknas om.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Att spara ett dokument till PDF, som en bild eller skriva ut för första gången kommer automatiskt
// cachelagrar dokumentets layout inom dess sidor.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

// Ändra dokumentet på något sätt.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

// I den nuvarande versionen av Aspose.Words återskapas inte dokumentet automatiskt när du ändrar det
// den cachade sidlayouten. Om vi önskar den cachade layouten
// för att hålla oss uppdaterade måste vi uppdatera den manuellt.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

### Se även

* class [Style](../../style/)
* class [StyleCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## StyleCollection indexer (2 of 3)

Hämtar en inbyggd stil genom sin språkoberoende identifierare.

```csharp
public Style this[StyleIdentifier sti] { get; }
```

| Parameter | Beskrivning |
| --- | --- |
| sti | En[`StyleIdentifier`](../../styleidentifier/) värde som anger den inbyggda stilen som ska hämtas. |

## Anmärkningar

När man öppnar en stil som ännu inte finns, skapas den automatiskt.

## Exempel

Visar hur man lägger till en stil i ett dokuments stilsamling.

```csharp
Document doc = new Document();

StyleCollection styles = doc.Styles;
// Ange standardparametrar för nya stilar som vi senare kan lägga till i den här samlingen.
styles.DefaultFont.Name = "Courier New";
// Om vi lägger till en stil av typen "StyleType.Paragraph" kommer samlingen att tillämpa värdena för
// dess "DefaultParagraphFormat"-egenskap till stilens "ParagraphFormat"-egenskap.
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;
// Lägg till en stil och kontrollera sedan att den har standardinställningarna.
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

### Se även

* class [Style](../../style/)
* enum [StyleIdentifier](../../styleidentifier/)
* class [StyleCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## StyleCollection indexer (3 of 3)

Hämtar en stil efter index.

```csharp
public Style this[int index] { get; }
```

## Exempel

Visar hur man lägger till en stil i ett dokuments stilsamling.

```csharp
Document doc = new Document();

StyleCollection styles = doc.Styles;
// Ange standardparametrar för nya stilar som vi senare kan lägga till i den här samlingen.
styles.DefaultFont.Name = "Courier New";
// Om vi lägger till en stil av typen "StyleType.Paragraph" kommer samlingen att tillämpa värdena för
// dess "DefaultParagraphFormat"-egenskap till stilens "ParagraphFormat"-egenskap.
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;
// Lägg till en stil och kontrollera sedan att den har standardinställningarna.
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

### Se även

* class [Style](../../style/)
* class [StyleCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
