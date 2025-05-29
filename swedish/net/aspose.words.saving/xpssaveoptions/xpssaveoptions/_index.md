---
title: XpsSaveOptions
linktitle: XpsSaveOptions
articleTitle: XpsSaveOptions
second_title: Aspose.Words för .NET
description: Upptäck konstruktorn XpsSaveOptions för att enkelt skapa instanser för att spara dokument i XPS-format, vilket förbättrar effektiviteten i din dokumenthantering.
type: docs
weight: 10
url: /sv/net/aspose.words.saving/xpssaveoptions/xpssaveoptions/
---
## XpsSaveOptions() {#constructor}

Initierar en ny instans av den här klassen som kan användas för att spara ett dokument iXps format.

```csharp
public XpsSaveOptions()
```

## Exempel

Visar hur man begränsar rubriknivån som visas i dispositionen i ett sparat XPS-dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga rubriker som kan fungera som innehållsförteckningsposter för nivå 1, 2 och sedan 3.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// Skapa ett "XpsSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .XPS.
XpsSaveOptions saveOptions = new XpsSaveOptions();

Assert.AreEqual(SaveFormat.Xps, saveOptions.SaveFormat);

// Det utgående XPS-dokumentet kommer att innehålla en disposition, en innehållsförteckning som listar rubriker i dokumentets brödtext.
// Om du klickar på en post i den här dispositionen kommer vi till platsen för respektive rubrik.
// Sätt egenskapen "HeadingsOutlineLevels" till "2" för att exkludera alla rubriker vars nivåer är över 2 från dispositionen.
// De två sista rubrikerna som vi har infogat ovan kommer inte att visas.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

### Se även

* class [XpsSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)

---

## XpsSaveOptions(*[SaveFormat](../../../aspose.words/saveformat/)*) {#constructor_1}

Initierar en ny instans av den här klassen som kan användas för att spara ett dokument iXps ellerOpenXps format.

```csharp
public XpsSaveOptions(SaveFormat saveFormat)
```

## Exempel

Visar hur man sparar ett dokument i XPS-format i form av en bokvikning.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Skapa ett "XpsSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .XPS.
XpsSaveOptions xpsOptions = new XpsSaveOptions(SaveFormat.Xps);

// Sätt egenskapen "UseBookFoldPrintingSettings" till "true" för att ordna innehållet
// i utdata-XPS:en på ett sätt som hjälper oss att använda den för att skapa ett häfte.
// Sätt egenskapen "UseBookFoldPrintingSettings" till "false" för att rendera XPS normalt.
xpsOptions.UseBookFoldPrintingSettings = renderTextAsBookFold;

// Om vi renderar dokumentet som ett häfte måste vi ställa in "Flera sidor"
// egenskaper för sidinställningar-objekten för alla sektioner till "MultiplePagesType.BookFoldPrinting".
if (renderTextAsBookFold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// När vi har skrivit ut det här dokumentet kan vi göra om det till ett häfte genom att stapla sidorna
// att komma ut ur skrivaren och vika ner på mitten.
doc.Save(ArtifactsDir + "XpsSaveOptions.BookFold.xps", xpsOptions);
```

### Se även

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [XpsSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
