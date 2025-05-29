---
title: HtmlSaveOptions.ExportLanguageInformation
linktitle: ExportLanguageInformation
articleTitle: ExportLanguageInformation
second_title: Aspose.Words för .NET
description: Styr språkexport i HTML, MHTML eller EPUB med HtmlSaveOptions. Förbättra dokumenttillgängligheten och nå en bredare publik utan ansträngning.
type: docs
weight: 180
url: /sv/net/aspose.words.saving/htmlsaveoptions/exportlanguageinformation/
---
## HtmlSaveOptions.ExportLanguageInformation property

Anger om språkinformation exporteras till HTML, MHTML eller EPUB. Standard är`falsk` .

```csharp
public bool ExportLanguageInformation { get; set; }
```

## Anmärkningar

När den här egenskapen är inställd på`sann` Aspose.Words-utdata**lång**HTML-attribut på document -elementen som anger språk. Detta kan behövas för att bevara språkrelaterad semantik.

## Exempel

Visar hur man bevarar språkinformation när man sparar till .html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Använd verktyget för att skriva text samtidigt som du formaterar den på olika språk.
builder.Font.LocaleId = new CultureInfo("en-US").LCID;
builder.Writeln("Hello world!");

builder.Font.LocaleId = new CultureInfo("en-GB").LCID;
builder.Writeln("Hello again!");

builder.Font.LocaleId = new CultureInfo("ru-RU").LCID;
builder.Write("Привет, мир!");

// När vi sparar dokumentet till HTML kan vi skicka ett SaveOptions-objekt
// för att antingen bevara eller ta bort varje formaterad texts språkinställning.
// Om vi ställer in flaggan "ExportLanguageInformation" till "sant",
// HTML-dokumentet som utdata kommer att innehålla språkinställningarna i "lang"-attributen för <span>-taggarna.
// Om vi ställer in flaggan "ExportLanguageInformation" till "false",
// texten i HTML-dokumentet som utdata kommer inte att innehålla någon språkinformation.
HtmlSaveOptions options = new HtmlSaveOptions
{
    ExportLanguageInformation = exportLanguageInformation,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportLanguageInformation.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportLanguageInformation.html");

if (exportLanguageInformation)
{
    Assert.True(outDocContents.Contains("<span>Hello world!</span>"));
    Assert.True(outDocContents.Contains("<span lang=\"en-GB\">Hello again!</span>"));
    Assert.True(outDocContents.Contains("<span lang=\"ru-RU\">Привет, мир!</span>"));
}
else
{
    Assert.True(outDocContents.Contains("<span>Hello world!</span>"));
    Assert.True(outDocContents.Contains("<span>Hello again!</span>"));
    Assert.True(outDocContents.Contains("<span>Привет, мир!</span>"));
}
```

### Se även

* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
