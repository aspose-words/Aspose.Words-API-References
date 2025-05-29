---
title: IStructuredDocumentTag.Tag
linktitle: Tag
articleTitle: Tag
second_title: Aspose.Words för .NET
description: Upptäck egenskapen IStructuredDocumentTag som definierar en unik tagg för din SDT-nod, vilket förbättrar dokumentstrukturen och säkerställer tydlighet.
type: docs
weight: 130
url: /sv/net/aspose.words.markup/istructureddocumenttag/tag/
---
## IStructuredDocumentTag.Tag property

Anger en tagg som är associerad med den aktuella SDT-noden. Kan inte vara null.

```csharp
public string Tag { get; set; }
```

## Exempel

Visar hur man skapar en strukturerad dokumenttagg i en vanlig textruta och ändrar dess utseende.

```csharp
Document doc = new Document();

// Skapa en strukturerad dokumenttagg som innehåller vanlig text.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Ange titel och färg på ramen som visas när du för muspekaren över taggen för det strukturerade dokumentet i Microsoft Word.
tag.Title = "My plain text";
tag.Color = Color.Magenta;

// Ange en tagg för denna strukturerade dokumenttagg, som är tillgänglig
// som ett XML-element med namnet "tag", med strängen nedan i dess "@val"-attribut.
tag.Tag = "MyPlainTextSDT";

// Varje tagg för ett strukturerat dokument har ett slumpmässigt unikt ID.
Assert.IsTrue(tag.Id > 0);

// Ange teckensnittet för texten inuti den strukturerade dokumenttaggen.
tag.ContentsFont.Name = "Arial";

// Ange teckensnittet för texten i slutet av den strukturerade dokumenttaggen.
// All text som vi skriver i dokumentets brödtext efter att ha flyttat oss ut ur taggen med piltangenterna kommer att använda detta teckensnitt.
tag.EndCharacterFont.Name = "Arial Black";

// Som standard är detta falskt och att trycka på Enter inuti en strukturerad dokumenttagg gör ingenting.
// När den är satt till sant kan vår strukturerade dokumenttagg ha flera rader.

// Sätt egenskapen "Multiline" till "false" för att endast tillåta innehållet
// av denna strukturerade dokumenttagg för att sträcka sig över en enda rad.
// Sätt egenskapen "Multiline" till "true" för att tillåta att taggen innehåller flera rader med innehåll.
tag.Multiline = true;

// Ställ in egenskapen "Appearance" till "SdtAppearance.Tags" för att visa taggar runt innehåll.
 // Som standard visas taggen för strukturerat dokument som BoundingBox.
tag.Appearance = SdtAppearance.Tags;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(tag);

// Infoga en klon av vår tagg för strukturerat dokument i ett nytt stycke.
StructuredDocumentTag tagClone = (StructuredDocumentTag)tag.Clone(true);
builder.InsertParagraph();
builder.InsertNode(tagClone);

// Använd metoden "RemoveSelfOnly" för att ta bort en strukturerad dokumenttagg, samtidigt som innehållet behålls i dokumentet.
tagClone.RemoveSelfOnly();

doc.Save(ArtifactsDir + "StructuredDocumentTag.PlainText.docx");
```

### Se även

* interface [IStructuredDocumentTag](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
