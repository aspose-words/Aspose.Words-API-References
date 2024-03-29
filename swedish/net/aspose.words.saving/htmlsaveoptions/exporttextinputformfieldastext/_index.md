---
title: HtmlSaveOptions.ExportTextInputFormFieldAsText
linktitle: ExportTextInputFormFieldAsText
articleTitle: ExportTextInputFormFieldAsText
second_title: Aspose.Words för .NET
description: HtmlSaveOptions ExportTextInputFormFieldAsText fast egendom. Styr hur formulärfält för textinmatning sparas i HTML eller MHTML. Standardvärdet ärfalsk  i C#.
type: docs
weight: 260
url: /sv/net/aspose.words.saving/htmlsaveoptions/exporttextinputformfieldastext/
---
## HtmlSaveOptions.ExportTextInputFormFieldAsText property

Styr hur formulärfält för textinmatning sparas i HTML eller MHTML. Standardvärdet är`falsk` .

```csharp
public bool ExportTextInputFormFieldAsText { get; set; }
```

## Anmärkningar

När inställd på`Sann` , exporterar textinmatningsformulärfält som normal text. När`falsk`, exporterar Word-textinmatningsfält som INPUT-element i HTML.

Vid export till EPUB sparas formulärfält för textinmatning alltid som text på grund av till kraven i detta format.

## Exempel

Visar hur man anger mappen för lagring av länkade bilder efter att ha sparats i .html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// Ställ in ett alternativ för att exportera formulärfält som vanlig text istället för HTML-inmatningselement.
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
