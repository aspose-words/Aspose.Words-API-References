---
title: StructuredDocumentTag.Multiline
second_title: Aspose.Words för .NET API Referens
description: StructuredDocumentTag fast egendom. Anger om detta SDT tillåter flera textrader.
type: docs
weight: 210
url: /sv/net/aspose.words.markup/structureddocumenttag/multiline/
---
## StructuredDocumentTag.Multiline property

Anger om detta **SDT** tillåter flera textrader.

```csharp
public bool Multiline { get; set; }
```

### Anmärkningar

Åtkomst till den här egenskapen fungerar bara förRichText ochPlainText SDT-typ.

För alla andra SDT-typer kommer undantag att förekomma.

### Exempel

Visar hur man skapar en strukturerad dokumenttagg i en vanlig textruta och ändrar dess utseende.

```csharp
Document doc = new Document();

// Skapa en strukturerad dokumenttagg som kommer att innehålla vanlig text.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Ställ in titeln och färgen på ramen som visas när du för musen över den strukturerade dokumenttaggen i Microsoft Word.
tag.Title = "My plain text";
tag.Color = Color.Magenta;

// Ställ in en tagg för denna strukturerade dokumenttagg, som är tillgänglig
// som ett XML-element med namnet "tag", med strängen nedan i dess "@val"-attribut.
tag.Tag = "MyPlainTextSDT";

// Varje strukturerad dokumenttagg har ett slumpmässigt unikt ID.
Assert.That(tag.Id, Is.Positive);

// Ställ in typsnittet för texten inuti den strukturerade dokumenttaggen.
tag.ContentsFont.Name = "Arial";

// Ställ in typsnittet för texten i slutet av den strukturerade dokumenttaggen.
// All text som vi skriver i dokumentets brödtext efter att ha flyttat ut ur taggen med piltangenterna kommer att använda detta teckensnitt.
tag.EndCharacterFont.Name = "Arial Black";

// Som standard är detta falskt och att trycka på enter när du är inne i en strukturerad dokumenttagg gör ingenting.
// När satt till true kan vår strukturerade dokumenttagg ha flera rader.

// Ställ in egenskapen "Multiline" till "false" för att bara tillåta innehållet
// av denna strukturerade dokumenttagg för att spänna över en enda rad.
// Ställ in egenskapen "Multiline" till "true" för att tillåta taggen att innehålla flera rader med innehåll.
tag.Multiline = true;

// Ställ in egenskapen "Appearance" till "SdtAppearance.Tags" för att visa taggar runt innehåll.
  // Som standard visas strukturerad dokumenttagg som BoundingBox.
tag.Appearance = SdtAppearance.Tags;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(tag);

// Infoga en klon av vår strukturerade dokumenttagg i ett nytt stycke.
StructuredDocumentTag tagClone = (StructuredDocumentTag)tag.Clone(true);
builder.InsertParagraph();
builder.InsertNode(tagClone);

// Använd metoden "RemoveSelfOnly" för att ta bort en strukturerad dokumenttagg, samtidigt som dess innehåll behålls i dokumentet.
tagClone.RemoveSelfOnly();

doc.Save(ArtifactsDir + "StructuredDocumentTag.PlainText.docx");
```

### Se även

* class [StructuredDocumentTag](../)
* namnutrymme [Aspose.Words.Markup](../../structureddocumenttag/)
* hopsättning [Aspose.Words](../../../)


