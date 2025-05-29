---
title: IStructuredDocumentTag.PlaceholderName
linktitle: PlaceholderName
articleTitle: PlaceholderName
second_title: Aspose.Words för .NET
description: Upptäck egenskapen IStructuredDocumentTag PlaceholderName för att enkelt hantera BuildingBlock-namn och förbättra dokumentets platshållartext.
type: docs
weight: 110
url: /sv/net/aspose.words.markup/istructureddocumenttag/placeholdername/
---
## IStructuredDocumentTag.PlaceholderName property

Hämtar eller anger namnet på[`BuildingBlock`](../../../aspose.words.buildingblocks/buildingblock/) innehåller platshållartext.

```csharp
public string PlaceholderName { get; set; }
```

### Undantag

| undantag | skick |
| --- | --- |
| InvalidOperationException | Kasta om Byggblock med detta namn[`Name`](../../../aspose.words.buildingblocks/buildingblock/name/) finns inte i[`GlossaryDocument`](../../../aspose.words/document/glossarydocument/). |

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

* interface [IStructuredDocumentTag](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
