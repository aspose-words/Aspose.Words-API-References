---
title: HtmlVersion Enum
linktitle: HtmlVersion
articleTitle: HtmlVersion
second_title: Aspose.Words för .NET
description: Upptäck enumereringen Aspose.Words.Saving.HtmlVersion för att optimera dokumentsparning i HTML- och MHTML-format, vilket förbättrar kompatibilitet och prestanda.
type: docs
weight: 5870
url: /sv/net/aspose.words.saving/htmlversion/
---
## HtmlVersion enumeration

Anger vilken HTML-version som används när dokumentet sparas tillHtml och Mhtml format.

```csharp
public enum HtmlVersion
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Xhtml | `0` | Sparar dokumentet i enlighet med XHTML 1.0 Transitional-standarden. |
| Html5 | `1` | Sparar dokumentet i enlighet med HTML 5-standarden. |

## Exempel

Visar hur man visar en DOCTYPE-rubrik när man konverterar dokument till övergångsstandarden Xhtml 1.0.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    HtmlVersion = HtmlVersion.Xhtml,
    ExportXhtmlTransitional = showDoctypeDeclaration,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportXhtmlTransitional.html", options);

// Vårt dokument kommer bara att innehålla en DOCTYPE-deklarationsrubrik om vi har satt flaggan "ExportXhtmlTransitional" till "true".
string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportXhtmlTransitional.html");
string newLine = Environment.NewLine;

if (showDoctypeDeclaration)
    Assert.True(outDocContents.Contains(
        $"<?xml version=\"1.0\" encoding=\"utf-8\" standalone=\"no\"?>{newLine}" +
        $"<!DOCTYPE html PUBLIC \"-//W3C//DTD XHTML 1.0 Transitional//EN\" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd\">{newLine}" +
        "<html xmlns=\"http://www.w3.org/1999/xhtml\">"));
else
    Assert.True(outDocContents.Contains("<html>"));
```

Visar hur man sparar ett dokument till en specifik version av HTML.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    HtmlVersion = htmlVersion,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.HtmlVersions.html", options);

// Våra HTML-dokument kommer att ha mindre skillnader för att vara kompatibla med olika HTML-versioner.
string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.HtmlVersions.html");

switch (htmlVersion)
{
    case HtmlVersion.Html5:
        Assert.True(outDocContents.Contains("<a id=\"_Toc76372689\"></a>"));
        Assert.True(outDocContents.Contains("<a id=\"_Toc76372689\"></a>"));
        Assert.True(outDocContents.Contains("<table style=\"padding:0pt; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
        break;
    case HtmlVersion.Xhtml:
        Assert.True(outDocContents.Contains("<a name=\"_Toc76372689\"></a>"));
        Assert.True(outDocContents.Contains("<ul type=\"disc\" style=\"margin:0pt; padding-left:0pt\">"));
        Assert.True(outDocContents.Contains("<table cellspacing=\"0\" cellpadding=\"0\" style=\"-aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\""));
        break;
}
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
