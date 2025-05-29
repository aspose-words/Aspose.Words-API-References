---
title: HtmlSaveOptions.ExportXhtmlTransitional
linktitle: ExportXhtmlTransitional
articleTitle: ExportXhtmlTransitional
second_title: Aspose.Words för .NET
description: Optimera din HTML med egenskapen HtmlSaveOptions ExportXhtmlTransitional. Kontrollera DOCTYPE-deklarationer för bättre kompatibilitet i HTML-, MHTML- och EPUB-format.
type: docs
weight: 280
url: /sv/net/aspose.words.saving/htmlsaveoptions/exportxhtmltransitional/
---
## HtmlSaveOptions.ExportXhtmlTransitional property

Anger om DOCTYPE-deklarationen ska skrivas när man sparar till HTML eller MHTML. När`sann` , skriver en DOCTYPE-deklaration i dokumentet före rotelementet. Standardvärdet är`falsk`. När du sparar till EPUB eller HTML5 (Html5 ) DOCTYPE -deklarationen skrivs alltid.

```csharp
public bool ExportXhtmlTransitional { get; set; }
```

## Anmärkningar

Aspose.Words skriver alltid välformad HTML oavsett denna inställning.

När`sann`, kommer början av HTML-utdatadokumentet att se ut så här:

Aspose.Words strävar efter att skapa XHTML enligt XHTML 1.0 Transitional-specifikationen, men utdata kommer inte alltid att valideras mot DTD:n. Vissa strukturer i ett Microsoft Word-dokument är svåra eller omöjliga att mappa till ett dokument som valideras mot XHTML-schemat. Till exempel tillåter inte XHTML kapslade listor (UL kan inte kapslas inuti ett annat UL-element), men i Microsoft Word-dokument förekommer listor på flera nivåer ganska ofta.

```csharp
<?xml version="1.0" encoding="utf-8" standalone="no" ?>
<!DOCTYPE html
      PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
```

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

### Se även

* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
