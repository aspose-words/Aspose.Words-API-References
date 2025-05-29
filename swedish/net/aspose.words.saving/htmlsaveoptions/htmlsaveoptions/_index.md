---
title: HtmlSaveOptions
linktitle: HtmlSaveOptions
articleTitle: HtmlSaveOptions
second_title: Aspose.Words för .NET
description: Upptäck HtmlSaveOptions-konstruktorn för att enkelt skapa och spara dokument i HTML-format, vilket säkerställer optimal formatering och enkel delning.
type: docs
weight: 10
url: /sv/net/aspose.words.saving/htmlsaveoptions/htmlsaveoptions/
---
## HtmlSaveOptions() {#constructor}

Initierar en ny instans av den här klassen som kan användas för att spara ett dokument iHtml format.

```csharp
public HtmlSaveOptions()
```

## Exempel

Visar hur man använder en specifik kodning när man sparar ett dokument till .epub.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Använd ett SaveOptions-objekt för att ange kodningen för ett dokument som vi ska spara.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// Som standard kommer ett .epub-dokument att ha allt innehåll i en HTML-del.
// Ett delningskriterium låter oss segmentera dokumentet i flera HTML-delar.
// Vi kommer att ställa in kriterierna för att dela upp dokumentet i rubrikstycken.
// Detta är användbart för läsare som inte kan läsa HTML-filer som är större än en viss storlek.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Ange att vi vill exportera dokumentegenskaper.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### Se även

* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)

---

## HtmlSaveOptions(*[SaveFormat](../../../aspose.words/saveformat/)*) {#constructor_1}

Initierar en ny instans av den här klassen som kan användas för att spara ett dokument iHtml ,Mhtml ,Epub , Azw3 ellerMobi format.

```csharp
public HtmlSaveOptions(SaveFormat saveFormat)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| saveFormat | SaveFormat | Kan varaHtml ,Mhtml ,Epub , Azw3 ellerMobi . |

## Exempel

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
