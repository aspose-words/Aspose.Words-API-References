---
title: HtmlSaveOptions.ExportXhtmlTransitional
second_title: Aspose.Words för .NET API Referens
description: HtmlSaveOptions fast egendom. Anger om DOCTYPEdeklarationen ska skrivas när du sparar till HTML eller MHTML. NärSann  skriver en DOCTYPEdeklaration i dokumentet före rotelementet. Standardvärdet ärfalsk. När du sparar till EPUB eller HTML5 Html5  DOCTYPE deklarationen skrivs alltid.
type: docs
weight: 290
url: /sv/net/aspose.words.saving/htmlsaveoptions/exportxhtmltransitional/
---
## HtmlSaveOptions.ExportXhtmlTransitional property

Anger om DOCTYPE-deklarationen ska skrivas när du sparar till HTML eller MHTML. När`Sann` , skriver en DOCTYPE-deklaration i dokumentet före rotelementet. Standardvärdet är`falsk`. När du sparar till EPUB eller HTML5 (Html5 ) DOCTYPE -deklarationen skrivs alltid.

```csharp
public bool ExportXhtmlTransitional { get; set; }
```

### Anmärkningar

Aspose.Words skriver alltid välformad HTML oavsett denna inställning.

När`Sann`, kommer början av HTML-utdatadokumentet att se ut så här:

Aspose.Words syftar till att mata ut XHTML enligt XHTML 1.0 Transitional-specifikationen, men utdata kommer inte alltid att valideras mot DTD. Vissa strukturer i ett Microsoft Word -dokument är svåra eller omöjliga att mappa till ett dokument som kommer att valideras mot XHTML-schemat. Till exempel tillåter inte XHTML kapslade listor (UL kan inte kapslas inuti ett annat UL-element), men i Microsoft Word-dokument förekommer flernivålistor ganska ofta.

```csharp
<?xml version="1.0" encoding="utf-8" standalone="no" ?>
<!DOCTYPE html 
      PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
```

### Exempel

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

if (showDoctypeDeclaration)
    Assert.True(outDocContents.Contains(
        "<?xml version=\"1.0\" encoding=\"utf-8\" standalone=\"no\"?>\r\n" +
        "<!DOCTYPE html PUBLIC \"-//W3C//DTD XHTML 1.0 Transitional//EN\" \"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd\">\r\n" +
        "<html xmlns=\"http://www.w3.org/1999/xhtml\">"));
else
    Assert.True(outDocContents.Contains("<html>"));
```

### Se även

* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../htmlsaveoptions/)
* hopsättning [Aspose.Words](../../../)


