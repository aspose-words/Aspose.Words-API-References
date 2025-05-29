---
title: ParagraphFormat.DropCapPosition
linktitle: DropCapPosition
articleTitle: DropCapPosition
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ParagraphFormat DropCapPosition för att enkelt anpassa din anfangstextplacering för förbättrad dokumentdesign och läsbarhet.
type: docs
weight: 100
url: /sv/net/aspose.words/paragraphformat/dropcapposition/
---
## ParagraphFormat.DropCapPosition property

Hämtar eller anger positionen för en anfangstext.

```csharp
public DropCapPosition DropCapPosition { get; set; }
```

## Exempel

Visar hur man kapslar en lista inuti en annan lista.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// En lista låter oss organisera och dekorera uppsättningar av stycken med prefixsymboler och indrag.
 // Vi kan skapa kapslade listor genom att öka indragsnivån.
 // Vi kan börja och avsluta en lista genom att använda dokumentbyggarens "ListFormat"-egenskap.
// Varje stycke som vi lägger till mellan en listas början och slut blir ett objekt i listan.
// Skapa en översiktslista för rubrikerna.
List outlineList = doc.Lists.Add(ListTemplate.OutlineNumbers);
builder.ListFormat.List = outlineList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("This is my Chapter 1");

// Skapa en numrerad lista.
List numberedList = doc.Lists.Add(ListTemplate.NumberDefault);
builder.ListFormat.List = numberedList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Normal;
builder.Writeln("Numbered list item 1.");

// Varje stycke som utgör en lista kommer att ha denna flagga.
Assert.True(builder.CurrentParagraph.IsListItem);
Assert.True(builder.ParagraphFormat.IsListItem);

// Skapa en punktlista.
List bulletedList = doc.Lists.Add(ListTemplate.BulletDefault);
builder.ListFormat.List = bulletedList;
builder.ParagraphFormat.LeftIndent = 72;
builder.Writeln("Bulleted list item 1.");
builder.Writeln("Bulleted list item 2.");
builder.ParagraphFormat.ClearFormatting();

// Återgå till den numrerade listan.
builder.ListFormat.List = numberedList;
builder.Writeln("Numbered list item 2.");
builder.Writeln("Numbered list item 3.");

// Återgå till dispositionslistan.
builder.ListFormat.List = outlineList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("This is my Chapter 2");

builder.ParagraphFormat.ClearFormatting();

builder.Document.Save(ArtifactsDir + "Lists.NestedLists.docx");
```

### Se även

* enum [DropCapPosition](../../dropcapposition/)
* class [ParagraphFormat](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
