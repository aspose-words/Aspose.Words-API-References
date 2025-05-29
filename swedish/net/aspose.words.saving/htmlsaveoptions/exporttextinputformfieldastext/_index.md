---
title: HtmlSaveOptions.ExportTextInputFormFieldAsText
linktitle: ExportTextInputFormFieldAsText
articleTitle: ExportTextInputFormFieldAsText
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen HtmlSaveOptions ExportTextInputFormFieldAsText optimerar textinmatningsfält för sömlös HTML- eller MHTML-sparning. Förbättra din exportprocess!
type: docs
weight: 260
url: /sv/net/aspose.words.saving/htmlsaveoptions/exporttextinputformfieldastext/
---
## HtmlSaveOptions.ExportTextInputFormFieldAsText property

Styr hur textinmatningsfält sparas i HTML eller MHTML. Standardvärdet är`falsk` .

```csharp
public bool ExportTextInputFormFieldAsText { get; set; }
```

## Anmärkningar

När den är inställd på`sann` , exporterar textinmatningsfält i formuläret som vanlig text. När`falsk`, exporterar Word-textinmatningsformulärfält som INPUT-element i HTML.

Vid export till EPUB sparas textinmatningsfält alltid som text på grund av kraven i detta format.

## Exempel

Visar hur man anger mappen för att lagra länkade bilder efter att de har sparats till .html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// Ange ett alternativ för att exportera formulärfält som vanlig text istället för HTML-inmatningselement.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    ExportTextInputFormFieldAsText = true, 
    ImagesFolder = imagesDir
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

### Se även

* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
