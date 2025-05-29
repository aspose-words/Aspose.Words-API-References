---
title: Story.LastParagraph
linktitle: LastParagraph
articleTitle: LastParagraph
second_title: Aspose.Words för .NET
description: Få enkelt åtkomst till det sista stycket i din berättelse med egenskapen Story LastParagraph, vilket förbättrar din hantering och redigeringsupplevelse.
type: docs
weight: 20
url: /sv/net/aspose.words/story/lastparagraph/
---
## Story.LastParagraph property

Hämtar det sista stycket i berättelsen.

```csharp
public Paragraph LastParagraph { get; }
```

## Exempel

Visar hur man flyttar markörpositionen för en DocumentBuilder till en specifik nod.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Run 1. ");

// Dokumentbyggaren har en markör som fungerar som en del av dokumentet
// där byggaren lägger till nya noder när vi använder dess dokumentkonstruktionsmetoder.
// Den här markören fungerar på samma sätt som den blinkande markören i Microsoft Word,
// och den hamnar också alltid direkt efter en nod som byggaren just infogat.
// För att lägga till innehåll i en annan del av dokumentet,
// vi kan flytta markören till en annan nod med metoden "Flytta till".
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.Runs[0]);
// Markören är nu framför noden som vi flyttade den till.
// Om du lägger till en andra körning infogas den framför den första körningen.
builder.Writeln("Run 2. ");

Assert.AreEqual("Run 2. \rRun 1.", doc.GetText().Trim());

// Flytta markören till slutet av dokumentet för att fortsätta lägga till text i slutet som tidigare.
builder.MoveTo(doc.LastSection.Body.LastParagraph);
builder.Writeln("Run 3. ");

Assert.AreEqual("Run 2. \rRun 1. \rRun 3.", doc.GetText().Trim());
```

### Se även

* class [Paragraph](../../paragraph/)
* class [Story](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
