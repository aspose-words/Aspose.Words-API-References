---
title: HtmlSaveOptions.ResolveFontNames
linktitle: ResolveFontNames
articleTitle: ResolveFontNames
second_title: Aspose.Words för .NET
description: HtmlSaveOptions ResolveFontNames fast egendom. Anger om teckensnittsfamiljnamn som används i dokumentet löses och ersätts enligt FontSettings när de skrivs i HTMLbaserade format i C#.
type: docs
weight: 410
url: /sv/net/aspose.words.saving/htmlsaveoptions/resolvefontnames/
---
## HtmlSaveOptions.ResolveFontNames property

Anger om teckensnittsfamiljnamn som används i dokumentet löses och ersätts enligt [`FontSettings`](../../../aspose.words/document/fontsettings/) när de skrivs i HTML-baserade format.

```csharp
public bool ResolveFontNames { get; set; }
```

## Anmärkningar

Som standard är det här alternativet inställt på`falsk` och teckensnittsfamiljnamn skrivs till HTML som specificerat i källdokument. Det är,[`FontSettings`](../../../aspose.words/document/fontsettings/) ignoreras och ingen upplösning eller substitution av teckensnittsfamiljenamn utförs.

Om det här alternativet är inställt på`Sann` , Aspose.Words använder[`FontSettings`](../../../aspose.words/document/fontsettings/) att lösa varje teckensnittsfamiljsnamn som anges i ett källdokument till namnet på en tillgänglig teckensnittsfamilj, genom att utföra teckensnittsersättning efter behov.

## Exempel

Visar hur du löser alla teckensnittsnamn innan du skriver dem till HTML.

```csharp
Document doc = new Document(MyDir + "Missing font.docx");

// Det här dokumentet innehåller text som namnger ett teckensnitt som vi inte har.
Assert.NotNull(doc.FontInfos["28 Days Later"]);

// Om vi inte har något sätt att få det här typsnittet, och vi vill kunna visa all text
// i det här dokumentet i en utdata-HTML kan vi ersätta det med ett annat typsnitt.
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
    // Som standard är det här alternativet inställt på 'False' och Aspose.Words skriver teckensnittsnamn som anges i källdokumentet
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
