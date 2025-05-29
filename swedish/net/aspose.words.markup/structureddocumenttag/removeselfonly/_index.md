---
title: StructuredDocumentTag.RemoveSelfOnly
linktitle: RemoveSelfOnly
articleTitle: RemoveSelfOnly
second_title: Aspose.Words för .NET
description: Upptäck StructuredDocumentTag RemoveSelfOnly-metoden för att enkelt eliminera en SDT-nod samtidigt som innehållet i ditt dokument bevaras. Förbättra din redigeringseffektivitet!
type: docs
weight: 370
url: /sv/net/aspose.words.markup/structureddocumenttag/removeselfonly/
---
## StructuredDocumentTag.RemoveSelfOnly method

Tar bort endast denna SDT-nod, men behåller dess innehåll i dokumentträdet.

```csharp
public void RemoveSelfOnly()
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

* class [StructuredDocumentTag](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
