---
title: HtmlSaveOptions.ExportPageSetup
linktitle: ExportPageSetup
articleTitle: ExportPageSetup
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen HtmlSaveOptions ExportPageSetup förbättrar dina HTML-, MHTML- eller EPUB-exporter genom att möjliggöra anpassningsbara sidinställningar för bättre resultat.
type: docs
weight: 220
url: /sv/net/aspose.words.saving/htmlsaveoptions/exportpagesetup/
---
## HtmlSaveOptions.ExportPageSetup property

Anger om utskriftsformatet exporteras till HTML, MHTML eller EPUB. Standard är`falsk` .

```csharp
public bool ExportPageSetup { get; set; }
```

## Anmärkningar

Varje[`Section`](../../../aspose.words/section/) I Aspose.Words-dokumentmodellen tillhandahålls information om sidinställningar via[`PageSetup`](../../../aspose.words/pagesetup/) klass. När du exporterar ett dokument till HTML-format kan du behöva spara denna information för vidare användning. Särskilt sidinställningar kan vara viktiga för rendering till sidformat (utskrift) eller efterföljande konvertering till de ursprungliga Microsoft Word-filformaten (DOCX, DOC, RTF, WML).

I de flesta fall är HTML avsett för visning i webbläsare där paginering inte utförs. Så den här funktionen är inaktiv som standard.

## Exempel

Visar hur man avgör om sektionsstruktur/sidinställningar ska bevaras när man sparar till HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");

PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.TopMargin = 36.0;
pageSetup.BottomMargin = 36.0;
pageSetup.PaperSize = PaperSize.A5;

// När vi sparar dokumentet till HTML kan vi skicka ett SaveOptions-objekt
// för att bestämma om inställningarna för sidinställningar ska behållas eller ignoreras.
// Om vi ställer in flaggan "ExportPageSetup" till "true" kommer HTML-dokumentet att innehålla vår konfiguration för sidinställningar.
// Om vi ställer in flaggan "ExportPageSetup" till "false" kommer sparåtgärden att ignorera våra sidinställningar.
// för det första avsnittet, och båda avsnitten kommer att se identiska ut.
HtmlSaveOptions options = new HtmlSaveOptions { ExportPageSetup = exportPageSetup };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportPageSetup.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportPageSetup.html");

if (exportPageSetup)
{
    Assert.True(outDocContents.Contains(
        "<style type=\"text/css\">" +
            "@page Section_1 { size:419.55pt 595.3pt; margin:36pt 70.85pt; -aw-footer-distance:35.4pt; -aw-header-distance:35.4pt }" +
            "@page Section_2 { size:612pt 792pt; margin:70.85pt; -aw-footer-distance:35.4pt; -aw-header-distance:35.4pt }" +
            "div.Section_1 { page:Section_1 }div.Section_2 { page:Section_2 }" +
        "</style>"));

    Assert.True(outDocContents.Contains(
        "<div class=\"Section_1\">" +
            "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                "<span>Section 1</span>" +
            "</p>" +
        "</div>"));
}
else
{
    Assert.False(outDocContents.Contains("style type=\"text/css\">"));

    Assert.True(outDocContents.Contains(
        "<div>" +
            "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                "<span>Section 1</span>" +
            "</p>" +
        "</div>"));
}
```

### Se även

* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
