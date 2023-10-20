---
title: DocumentBuilder.MoveToParagraph
linktitle: MoveToParagraph
articleTitle: MoveToParagraph
second_title: Aspose.Words för .NET
description: DocumentBuilder MoveToParagraph metod. Flyttar markören till ett stycke i det aktuella avsnittet i C#.
type: docs
weight: 560
url: /sv/net/aspose.words/documentbuilder/movetoparagraph/
---
## DocumentBuilder.MoveToParagraph method

Flyttar markören till ett stycke i det aktuella avsnittet.

```csharp
public void MoveToParagraph(int paragraphIndex, int characterIndex)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| paragraphIndex | Int32 | Indexet för stycket att flytta till. |
| characterIndex | Int32 | Indexet för tecknet inuti stycket. Ett negativt värde låter dig ange en position från slutet av stycket. Använd -1 för att flytta till slutet av stycket. |

## Anmärkningar

Navigeringen utförs i den aktuella berättelsen i det aktuella avsnittet. Det vill säga om du flyttade markören till den primära rubriken i den första sektionen, då*paragraphIndex*specificerade indexet för stycket inuti header i det avsnittet.

När*paragraphIndex* är större än eller lika med 0, anger det ett index från början av avsnittet med 0 som första stycket. När*paragraphIndex* är mindre än 0, den specificerade ett index från slutet av avsnittet med -1 som det sista stycket.

## Exempel

Visar hur man flyttar en byggares markörposition till ett angivet stycke.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(22, paragraphs.Count);

// Skapa dokumentbyggare för att redigera dokumentet. Byggarens markör,
// vilket är den punkt där den kommer att infoga nya noder när vi anropar dess dokumentkonstruktionsmetoder,
// är för närvarande i början av dokumentet.
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.AreEqual(0, paragraphs.IndexOf(builder.CurrentParagraph));

// Flytta markören till ett annat stycke kommer att placera markören framför det stycket.
builder.MoveToParagraph(2, 0);
// Allt nytt innehåll som vi lägger till kommer att infogas vid den tidpunkten.
builder.Writeln("This is a new third paragraph. ");
```

### Se även

* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
