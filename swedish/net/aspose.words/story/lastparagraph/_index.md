---
title: Story.LastParagraph
second_title: Aspose.Words för .NET API Referens
description: Story fast egendom. Hämtar det sista stycket i berättelsen.
type: docs
weight: 20
url: /sv/net/aspose.words/story/lastparagraph/
---
## Story.LastParagraph property

Hämtar det sista stycket i berättelsen.

```csharp
public Paragraph LastParagraph { get; }
```

### Exempel

Visar hur man flyttar en DocumentBuilders markörposition till en angiven nod.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Run 1. ");

// Dokumentbyggaren har en markör, som fungerar som en del av dokumentet
// där byggaren lägger till nya noder när vi använder dess dokumentkonstruktionsmetoder.
// Den här markören fungerar på samma sätt som Microsoft Words blinkande markör,
// och det hamnar också alltid omedelbart efter någon nod som byggaren precis infogat.
// För att lägga till innehåll till en annan del av dokumentet,
// vi kan flytta markören till en annan nod med "MoveTo"-metoden.
// Markören är nu framför noden som vi flyttade den till.
// Om du lägger till en andra körning infogas den framför den första körningen.
builder.Writeln("Run 2. ");

Assert.AreEqual("Run 2. \rRun 1.", doc.GetText().Trim());

// Flytta markören till slutet av dokumentet för att fortsätta lägga till text till slutet som tidigare.
builder.MoveTo(doc.LastSection.Body.LastParagraph);
builder.Writeln("Run 3. ");

Assert.AreEqual("Run 2. \rRun 1. \rRun 3.", doc.GetText().Trim());
```

### Se även

* class [Paragraph](../../paragraph/)
* class [Story](../)
* namnutrymme [Aspose.Words](../../story/)
* hopsättning [Aspose.Words](../../../)


