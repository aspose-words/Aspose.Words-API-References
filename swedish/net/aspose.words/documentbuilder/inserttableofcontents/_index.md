---
title: DocumentBuilder.InsertTableOfContents
linktitle: InsertTableOfContents
articleTitle: InsertTableOfContents
second_title: Aspose.Words för .NET
description: DocumentBuilder InsertTableOfContents metod. Infogar ett TOCfält innehållsförteckning i dokumentet i C#.
type: docs
weight: 460
url: /sv/net/aspose.words/documentbuilder/inserttableofcontents/
---
## DocumentBuilder.InsertTableOfContents method

Infogar ett TOC-fält (innehållsförteckning) i dokumentet.

```csharp
public Field InsertTableOfContents(string switches)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| switches | String | TOC-fältet växlar. |

## Anmärkningar

Denna metod infogar ett TOC-fält (innehållsförteckning) i dokumentet vid den aktuella positionen.

En innehållsförteckning i ett Word-dokument kan byggas på ett antal sätt och formateras med en mängd olika alternativ. Hur tabellen är byggd och visas av Microsoft Word styrs av fältomkopplarna.

Det enklaste sättet att specificera växlarna är att infoga och konfigurera en tabell med innehåll i ett Word-dokument med hjälp av menyn Infoga-&gt;Referens-&gt;Index och tabeller, och sedan slå på visningen av fältkoder för att se växlarna. Du kan trycka på Alt+F9 in Microsoft Word för att växla visning av fältkoder på eller av.

Till exempel, efter att ha skapat en innehållsförteckning, infogas följande fält i dokumentet:**{ TOC \o "1-3" \h \z \u }** . Du kan kopiera**\o "1-3" \h \z \u** och använd den som switchparameter.

Anteckna det`InsertTableOfContents` kommer bara att infoga ett TOC-fält, men kommer faktiskt inte att bygga innehållsförteckningen. Innehållsförteckningen byggs av Microsoft Word när fältet uppdateras.

Om du infogar en innehållsförteckning med den här metoden och sedan öppnar filen i Microsoft Word, kommer du inte att se innehållsförteckningen eftersom TOC-fältet ännu inte har uppdaterats.

I Microsoft Word uppdateras inte fält automatiskt när ett dokument öppnas, men du kan när som helst uppdatera fält i ett dokument genom att trycka på F9.

## Exempel

Visar hur man infogar en innehållsförteckning (TOC) i ett dokument med rubrikstilar som poster.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga en innehållsförteckning för dokumentets första sida.
// Konfigurera tabellen för att ta upp stycken med rubriker på nivå 1 till 3.
// Ställ också in dess poster att vara hyperlänkar som tar oss
// till platsen för rubriken när du vänsterklickar i Microsoft Word.
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Fyll i innehållsförteckningen genom att lägga till stycken med rubrikstilar.
// Varje sådan rubrik med en nivå mellan 1 och 3 kommer att skapa en post i tabellen.
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
