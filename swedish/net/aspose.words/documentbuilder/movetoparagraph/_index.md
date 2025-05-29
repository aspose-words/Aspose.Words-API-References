---
title: DocumentBuilder.MoveToParagraph
linktitle: MoveToParagraph
articleTitle: MoveToParagraph
second_title: Aspose.Words för .NET
description: Navigera enkelt i ditt dokument med DocumentBuilder MoveToParagraph-metoden, vilket möjliggör snabb markörförflyttning till valfritt stycke i ditt avsnitt.
type: docs
weight: 600
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
| characterIndex | Int32 | Index för tecknet inuti stycket. Ett negativt värde låter dig ange en position från slutet av stycket. Använd -1 för att flytta till slutet av stycket. |

## Anmärkningar

Navigeringen utförs inom den aktuella artikeln i det aktuella avsnittet. Det vill säga, om du flyttade markören till den primära rubriken i det första avsnittet, så*paragraphIndex* angav indexet för stycket inuti header i det avsnittet.

När*paragraphIndex* är större än eller lika med 0, anger den ett index från början av avsnittet där 0 är det första stycket. När*paragraphIndex* är mindre än 0, specificerade det ett index från slutet av avsnittet där -1 är det sista stycket.

## Exempel

Visar hur man flyttar en verktygsbyggares markörposition till ett angivet stycke.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(22, paragraphs.Count);

// Skapa dokumentbyggaren för att redigera dokumentet. Byggarens markör,
// vilket är den punkt där den kommer att infoga nya noder när vi anropar dess dokumentkonstruktionsmetoder,
// är för närvarande i början av dokumentet.
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.AreEqual(0, paragraphs.IndexOf(builder.CurrentParagraph));

// Om du flyttar markören till ett annat stycke placeras markören framför det stycket.
builder.MoveToParagraph(2, 0);
// Allt nytt innehåll som vi lägger till kommer att infogas vid den tidpunkten.
builder.Writeln("This is a new third paragraph. ");
```

### Se även

* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
