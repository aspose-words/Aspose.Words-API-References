---
title: HtmlSaveOptions.ExportLanguageInformation
linktitle: ExportLanguageInformation
articleTitle: ExportLanguageInformation
second_title: Aspose.Words för .NET
description: HtmlSaveOptions ExportLanguageInformation fast egendom. Anger om språkinformation exporteras till HTML MHTML eller EPUB. Standard ärfalsk  i C#.
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

När den här egenskapen är inställd på`Sann` Aspose.Words-utgångar**lang** HTML-attribut på elementen document som anger språk. Detta kan behövas för att bevara språkrelaterad semantik.

## Exempel

Visar hur du bevarar språkinformation när du sparar till .html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Använd byggaren för att skriva text medan du formaterar den på olika språk.
builder.Font.LocaleId = new CultureInfo("en-US").LCID;
builder.Writeln("Hello world!");

builder.Font.LocaleId = new CultureInfo("en-GB").LCID;
builder.Writeln("Hello again!");

builder.Font.LocaleId = new CultureInfo("ru-RU").LCID;
builder.Write("Привет, мир!");

// När vi sparar dokumentet till HTML kan vi skicka ett SaveOptions-objekt
// för att antingen bevara eller förkasta varje formaterad texts språkkod.
// Om vi ställer in flaggan "ExportLanguageInformation" till "true",
// HTML-dokumentet kommer att innehålla språken i "lang"-attribut för <span> taggar.
// Om vi ställer in flaggan "ExportLanguageInformation" till "false",
// texten i HTML-dokumentet kommer inte att innehålla någon lokalinformation.
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
