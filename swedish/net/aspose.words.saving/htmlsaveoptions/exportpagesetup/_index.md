---
title: HtmlSaveOptions.ExportPageSetup
second_title: Aspose.Words för .NET API Referens
description: HtmlSaveOptions fast egendom. Anger om sidinställningarna exporteras till HTML MHTML eller EPUB. Standard ärfalsk .
type: docs
weight: 220
url: /sv/net/aspose.words.saving/htmlsaveoptions/exportpagesetup/
---
## HtmlSaveOptions.ExportPageSetup property

Anger om sidinställningarna exporteras till HTML, MHTML eller EPUB. Standard är`falsk` .

```csharp
public bool ExportPageSetup { get; set; }
```

### Anmärkningar

Varje[`Section`](../../../aspose.words/section/) i Aspose.Words dokumentmodell ger sidinställningar information via[`PageSetup`](../../../aspose.words/pagesetup/) klass. När du exporterar ett dokument till HTML-format kan du behöva behålla denna information för vidare användning. I synnerhet kan sidinställningarna vara viktiga för rendering till sidmedia (utskrift) eller efterföljande konvertering till de ursprungliga Microsoft Word-filformaten (DOCX, DOC, RTF, WML).

de flesta fall är HTML avsedd för visning i webbläsare där paginering inte utförs. Så denna feature är inaktiv som standard.

### Exempel

Visar hur du bestämmer om du vill behålla information om avsnittsstruktur/sidinställningar när du sparar till HTML.

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
// för att bestämma om sidinställningarna ska bevaras eller ignoreras.
// Om vi ställer in flaggan "ExportPageSetup" till "true", kommer HTML-dokumentet att innehålla vår sidinställningar.
// Om vi ställer in "ExportPageSetup"-flaggan till "false", kommer sparoperationen att ignorera våra sidinställningar
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
* namnutrymme [Aspose.Words.Saving](../../htmlsaveoptions/)
* hopsättning [Aspose.Words](../../../)


