---
title: XpsSaveOptions.XpsSaveOptions
second_title: Aspose.Words för .NET API Referens
description: XpsSaveOptions byggare. Initierar en ny instans av denna klass som kan användas för att spara ett document iXps format.
type: docs
weight: 10
url: /sv/net/aspose.words.saving/xpssaveoptions/xpssaveoptions/
---
## XpsSaveOptions() {#constructor}

Initierar en ny instans av denna klass som kan användas för att spara ett document iXps format.

```csharp
public XpsSaveOptions()
```

### Exempel

Visar hur man begränsar rubrikernas nivå som visas i konturerna av ett sparat XPS-dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga rubriker som kan fungera som TOC-poster på nivåerna 1, 2 och sedan 3.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// Skapa ett "XpsSaveOptions"-objekt som vi kan skicka till dokumentets "Spara"-metod
// för att ändra hur den metoden konverterar dokumentet till .XPS.
XpsSaveOptions saveOptions = new XpsSaveOptions();

Assert.AreEqual(SaveFormat.Xps, saveOptions.SaveFormat);

// XPS-dokumentet kommer att innehålla en disposition, en innehållsförteckning som listar rubriker i dokumentets brödtext.
// Genom att klicka på en post i denna disposition kommer vi till platsen för dess respektive rubrik.
// Ställ in egenskapen "HeadingsOutlineLevels" till "2" för att utesluta alla rubriker vars nivåer är över 2 från dispositionen.
// De två sista rubrikerna vi har infogat ovan kommer inte att visas.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

### Se även

* class [XpsSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../xpssaveoptions/)
* hopsättning [Aspose.Words](../../../)

---

## XpsSaveOptions(SaveFormat) {#constructor_1}

Initierar en ny instans av denna klass som kan användas för att spara ett document iXps ellerOpenXps format.

```csharp
public XpsSaveOptions(SaveFormat saveFormat)
```

### Exempel

Visar hur man sparar ett dokument i XPS-format i form av en bokvikning.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Skapa ett "XpsSaveOptions"-objekt som vi kan skicka till dokumentets "Spara"-metod
// för att ändra hur den metoden konverterar dokumentet till .XPS.
XpsSaveOptions xpsOptions = new XpsSaveOptions(SaveFormat.Xps);

// Ställ in egenskapen "UseBookFoldPrintingSettings" till "true" för att ordna innehållet
// i output XPS på ett sätt som hjälper oss att använda det för att göra ett häfte.
// Ställ in egenskapen "UseBookFoldPrintingSettings" till "false" för att rendera XPS normalt.
xpsOptions.UseBookFoldPrintingSettings = renderTextAsBookFold;

// Om vi renderar dokumentet som ett häfte måste vi ställa in "Flera sidor"
// egenskaper för sidinställningarna för alla sektioner till "MultiplePagesType.BookFoldPrinting".
if (renderTextAsBookFold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// När vi har skrivit ut det här dokumentet kan vi förvandla det till ett häfte genom att stapla sidorna
// för att komma ut ur skrivaren och fälla ner på mitten.
doc.Save(ArtifactsDir + "XpsSaveOptions.BookFold.xps", xpsOptions);
```

### Se även

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [XpsSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../xpssaveoptions/)
* hopsättning [Aspose.Words](../../../)


