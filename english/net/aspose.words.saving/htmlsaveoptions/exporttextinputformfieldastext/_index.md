---
title: HtmlSaveOptions.ExportTextInputFormFieldAsText
linktitle: ExportTextInputFormFieldAsText
second_title: Aspose.Words for .NET API Reference
description: HtmlSaveOptions property. Controls how text input form fields are saved to HTML or MHTML. Default value is false in C#.
type: docs
weight: 270
url: /net/aspose.words.saving/htmlsaveoptions/exporttextinputformfieldastext/
---
## HtmlSaveOptions.ExportTextInputFormFieldAsText property

Controls how text input form fields are saved to HTML or MHTML. Default value is `false`.

```csharp
public bool ExportTextInputFormFieldAsText { get; set; }
```

## Remarks

When set to `true`, exports text input form fields as normal text. When `false`, exports Word text input form fields as INPUT elements in HTML.

When exporting to EPUB, text input form fields are always saved as text due to requirements of this format.

## Examples

Shows how to specify the folder for storing linked images after saving to .html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// Set an option to export form fields as plain text instead of HTML input elements.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    ExportTextInputFormFieldAsText = true, 
    ImagesFolder = imagesDir
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

### See Also

* class [HtmlSaveOptions](../)
* namespace [Aspose.Words.Saving](../../htmlsaveoptions/)
* assembly [Aspose.Words](../../../)
