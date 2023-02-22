---
title: ParagraphFormat.SuppressLineNumbers
second_title: Aspose.Words för .NET API Referens
description: ParagraphFormat fast egendom. Anger om det aktuella styckets rader ska undantas från radnumrering som tillämpas i det överordnade avsnittet.
type: docs
weight: 370
url: /sv/net/aspose.words/paragraphformat/suppresslinenumbers/
---
## ParagraphFormat.SuppressLineNumbers property

Anger om det aktuella styckets rader ska undantas från radnumrering som tillämpas i det överordnade avsnittet.

```csharp
public bool SuppressLineNumbers { get; set; }
```

### Exempel

Visar hur man aktiverar radnumrering för en sektion.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Vi kan använda sektionens PageSetup-objekt för att visa siffror till vänster om sektionens textrader.
// Detta är samma beteende som ett List-objekt,
// men det täcker hela avsnittet och ändrar inte texten på något sätt.
// Vår sektion kommer att starta om numreringen på varje ny sida från 1 och visa numret,
// om det är en multipel av 3, vid 50pt till vänster om linjen.
PageSetup pageSetup = builder.PageSetup;
pageSetup.LineStartingNumber = 1;
pageSetup.LineNumberCountBy = 3;
pageSetup.LineNumberRestartMode = LineNumberRestartMode.RestartPage;
pageSetup.LineNumberDistanceFromText = 50.0d;

for (int i = 1; i <= 25; i++)
    builder.Writeln($"Line {i}.");

// Radräknaren hoppar över alla stycken med flaggan "SuppressLineNumbers" inställd på "true".
// Detta stycke är på den 15:e raden, vilket är en multipel av 3, och skulle därför normalt visa ett radnummer.
// Sektionens radräknare kommer också att ignorera denna rad, behandla nästa rad som den 15:e,
// och fortsätt räkningen från den punkten och framåt.
doc.FirstSection.Body.Paragraphs[14].ParagraphFormat.SuppressLineNumbers = true;

doc.Save(ArtifactsDir + "PageSetup.LineNumbers.docx");
```

### Se även

* class [ParagraphFormat](../)
* namnutrymme [Aspose.Words](../../paragraphformat/)
* hopsättning [Aspose.Words](../../../)


