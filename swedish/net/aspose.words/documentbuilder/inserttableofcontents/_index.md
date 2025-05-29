---
title: DocumentBuilder.InsertTableOfContents
linktitle: InsertTableOfContents
articleTitle: InsertTableOfContents
second_title: Aspose.Words för .NET
description: Förbättra dina dokument enkelt med DocumentBuilder-metoden InsertTableOfContents, och lägg till en dynamisk innehållsförteckning för enkel navigering och förbättrad organisation.
type: docs
weight: 500
url: /sv/net/aspose.words/documentbuilder/inserttableofcontents/
---
## DocumentBuilder.InsertTableOfContents method

Infogar ett innehållsförteckningsfält i dokumentet.

```csharp
public Field InsertTableOfContents(string switches)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| switches | String | Innehållsförteckningsfältet växlar. |

## Anmärkningar

Den här metoden infogar ett innehållsförteckningsfält (TOC) i dokumentet vid den aktuella positionen .

En innehållsförteckning i ett Word-dokument kan byggas på flera olika sätt och formateras med hjälp av en mängd olika alternativ. Hur tabellen byggs upp och visas i Microsoft Word styrs av fältväxlarna.

Det enklaste sättet att ange växlarna är att infoga och konfigurera en innehållsförteckning i ett Word-dokument med hjälp av menyn Infoga-&gt;Referens-&gt;Index och tabeller, och sedan slå på visning av fältkoder för att se växlarna. Du kan trycka på Alt+F9 i Microsoft Word för att slå på eller av visning av fältkoder.

Till exempel, efter att en innehållsförteckning har skapats, infogas följande fält i dokumentet:**{ INNEHÅLLSFÖRSLAG \o "1-3" \h \z \u }** . Du kan kopiera**\o "1-3" \h \z \u** och använd den som switches-parameter.

Observera att`InsertTableOfContents` infogar bara ett innehållsförteckningsfält, men kommer inte att bygga innehållsförteckningen. Innehållsförteckningen byggs av Microsoft Word när fältet uppdateras.

Om du infogar en innehållsförteckning med den här metoden och sedan öppnar filen i Microsoft Word, kommer du inte att se innehållsförteckningen eftersom innehållsförteckningsfältet ännu inte har uppdaterats.

I Microsoft Word uppdateras inte fält automatiskt när ett dokument öppnas, men du kan uppdatera fält i ett dokument när som helst genom att trycka på F9.

## Exempel

Visar hur man infogar en innehållsförteckning (TOC) i ett dokument med hjälp av rubrikformat som poster.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga en innehållsförteckning för dokumentets första sida.
// Konfigurera tabellen för att hämta stycken med rubriker på nivå 1 till 3.
// Ställ också in dess poster som hyperlänkar som tar oss
// till rubrikens plats när man vänsterklickar i Microsoft Word.
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Fyll innehållsförteckningen genom att lägga till stycken med rubrikformat.
// Varje sådan rubrik med en nivå mellan 1 och 3 skapar en post i tabellen.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 2");
builder.Writeln("Heading 3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;
builder.Writeln("Heading 3.1.1");
builder.Writeln("Heading 3.1.2");
builder.Writeln("Heading 3.1.3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;
builder.Writeln("Heading 3.1.3.1");
builder.Writeln("Heading 3.1.3.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.2");
builder.Writeln("Heading 3.3");

// En innehållsförteckning är ett fält av en typ som behöver uppdateras för att visa ett aktuellt resultat.
doc.UpdateFields();
doc.Save(ArtifactsDir + "DocumentBuilder.InsertToc.docx");
```

### Se även

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
