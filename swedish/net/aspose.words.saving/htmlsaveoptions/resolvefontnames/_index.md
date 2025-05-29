---
title: HtmlSaveOptions.ResolveFontNames
linktitle: ResolveFontNames
articleTitle: ResolveFontNames
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen HtmlSaveOptions ResolveFontNames förbättrar dokumentformatering genom att säkerställa korrekta teckensnittsersättningar i HTML-utdata.
type: docs
weight: 430
url: /sv/net/aspose.words.saving/htmlsaveoptions/resolvefontnames/
---
## HtmlSaveOptions.ResolveFontNames property

Anger om teckensnittsfamiljenamn som används i dokumentet är upplösta och ersatta enligt [`FontSettings`](../../../aspose.words/document/fontsettings/) när det skrivs till HTML-baserade format.

```csharp
public bool ResolveFontNames { get; set; }
```

## Anmärkningar

Som standard är det här alternativet inställt på`falsk` och teckensnittsfamiljenamn skrivs till HTML enligt specifikationerna i källdokumenten. Det vill säga,[`FontSettings`](../../../aspose.words/document/fontsettings/) ignoreras och ingen upplösning eller substitution av teckensnittsfamiljenamn utförs.

Om det här alternativet är inställt på`sann` , Aspose.Words använder[`FontSettings`](../../../aspose.words/document/fontsettings/) för att omvandla varje teckensnittsfamiljnamn som anges i ett källdokument till namnet på en tillgänglig teckensnittsfamilj, och utföra teckensnittsersättning efter behov.

## Exempel

Visar hur man löser alla typsnittsnamn innan man skriver dem till HTML.

```csharp
Document doc = new Document(MyDir + "Missing font.docx");

// Det här dokumentet innehåller text som namnger ett typsnitt som vi inte har.
Assert.NotNull(doc.FontInfos["28 Days Later"]);

// Om vi inte har något sätt att få tag på det här teckensnittet, och vi vill kunna visa all text
// i det här dokumentet i en utdata-HTML kan vi ersätta det med ett annat teckensnitt.
FontSettings fontSettings = new FontSettings
{
    SubstitutionSettings =
    {
        DefaultFontSubstitution =
        {
            DefaultFontName = "Arial",
            Enabled = true
        }
    }
};

doc.FontSettings = fontSettings;

HtmlSaveOptions saveOptions = new HtmlSaveOptions(SaveFormat.Html)
{
    // Som standard är det här alternativet inställt på 'False' och Aspose.Words skriver teckensnittsnamn som anges i källdokumentet.
    ResolveFontNames = resolveFontNames
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ResolveFontNames.html", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ResolveFontNames.html");

Assert.True(resolveFontNames
    ? Regex.Match(outDocContents, "<span style=\"font-family:Arial\">").Success
    : Regex.Match(outDocContents, "<span style=\"font-family:\'28 Days Later\'\">").Success);
```

### Se även

* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
