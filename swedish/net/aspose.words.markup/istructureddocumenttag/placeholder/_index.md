---
title: IStructuredDocumentTag.Placeholder
linktitle: Placeholder
articleTitle: Placeholder
second_title: Aspose.Words för .NET
description: Upptäck platshållaregenskapen IStructuredDocumentTag. Hantera enkelt platshållartext för tomt SDT-innehåll och förbättra dokumentets användbarhet.
type: docs
weight: 100
url: /sv/net/aspose.words.markup/istructureddocumenttag/placeholder/
---
## IStructuredDocumentTag.Placeholder property

Hämtar[`BuildingBlock`](../../../aspose.words.buildingblocks/buildingblock/) innehåller platshållartext som ska visas när innehållet i denna SDT-körning är tomt, det associerade mappade XML-elementet är tomt enligt anvisningarna via[`XmlMapping`](../xmlmapping/) element eller[`IsShowingPlaceholderText`](../isshowingplaceholdertext/) elementet är sant.

```csharp
public BuildingBlock Placeholder { get; }
```

## Anmärkningar

Kan vara null, vilket betyder att platshållaren inte är tillämplig för denna Sdt.

## Exempel

Visar hur man använder innehållet i ett byggblock som en anpassad platshållartext för en strukturerad dokumenttagg.

```csharp
Document doc = new Document();

// Infoga en tagg för ett strukturerat dokument med vanlig text av typen "PlainText", som fungerar som en textruta.
// Innehållet som visas som standard är en "Klicka här för att ange text."-prompt.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Vi kan få taggen att visa innehållet i ett byggblock istället för standardtexten.
// Lägg först till en byggsten med innehåll i ordlistadokumentet.
GlossaryDocument glossaryDoc = doc.GlossaryDocument;

BuildingBlock substituteBlock = new BuildingBlock(glossaryDoc);
substituteBlock.Name = "Custom Placeholder";
substituteBlock.AppendChild(new Section(glossaryDoc));
substituteBlock.FirstSection.AppendChild(new Body(glossaryDoc));
substituteBlock.FirstSection.Body.AppendParagraph("Custom placeholder text.");

glossaryDoc.AppendChild(substituteBlock);

// Använd sedan egenskapen "PlaceholderName" i taggen för strukturerat dokument för att referera till byggblocket med namn.
tag.PlaceholderName = "Custom Placeholder";

// Om "PlaceholderName" refererar till ett befintligt block i det överordnade dokumentets ordlista,
// vi kommer att kunna verifiera byggblocket via egenskapen "Platshållare".
Assert.AreEqual(substituteBlock, tag.Placeholder);

// Sätt egenskapen "IsShowingPlaceholderText" till "true" för att behandla
// strukturerad dokumenttaggs aktuella innehåll som platshållartext.
// Det här innebär att om du klickar på textrutan i Microsoft Word markeras allt innehåll i taggen omedelbart.
// Sätt egenskapen "IsShowingPlaceholderText" till "false" för att få
// strukturerad dokumenttagg för att behandla dess innehåll som text som en användare redan har angett.
// Om du klickar på den här texten i Microsoft Word placeras den blinkande markören på den plats där du klickade.
tag.IsShowingPlaceholderText = isShowingPlaceholderText;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.PlaceholderBuildingBlock.docx");
```

### Se även

* class [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/)
* interface [IStructuredDocumentTag](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
