---
title: HtmlFixedSaveOptions.ExportFormFields
second_title: Aspose.Words för .NET API Referens
description: HtmlFixedSaveOptions fast egendom. Hämtar eller ställer in en indikation på om formulärfält exporteras som interactive objekt som inputtagg snarare än omvandlas till text eller grafik.
type: docs
weight: 80
url: /sv/net/aspose.words.saving/htmlfixedsaveoptions/exportformfields/
---
## HtmlFixedSaveOptions.ExportFormFields property

Hämtar eller ställer in en indikation på om formulärfält exporteras som interactive objekt (som "input"-tagg) snarare än omvandlas till text eller grafik.

```csharp
public bool ExportFormFields { get; set; }
```

### Exempel

Visar hur man exporterar formulärfält till HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertCheckBox("CheckBox", false, 15);

// När vi exporterar ett dokument med formulärfält till .html,
// det finns två sätt på vilka Aspose.Words kan exportera formulärfält.
// Att ställa in "ExportFormFields"-flaggan till "true" kommer att exportera dem som interaktiva objekt.
// Om du ställer in denna flagga på "false" visas formulärfält som vanlig text.
// Detta kommer att frysa dem till deras nuvarande värde och hindra läsaren av vårt HTML-dokument
// från att kunna interagera med dem.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportFormFields = exportFormFields
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportFormFields.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportFormFields.html");

if (exportFormFields)
{
    Assert.True(Regex.Match(outDocContents,
        "<a name=\"CheckBox\" style=\"left:0pt; top:0pt;\"></a>" +
        "<input style=\"position:absolute; left:0pt; top:0pt;\" type=\"checkbox\" name=\"CheckBox\" />").Success);
}
else
{
    Assert.True(Regex.Match(outDocContents, 
        "<a name=\"CheckBox\" style=\"left:0pt; top:0pt;\"></a>" +
        "<div class=\"awdiv\" style=\"left:0.8pt; top:0.8pt; width:14.25pt; height:14.25pt; border:solid 0.75pt #000000;\"").Success);
}
```

### Se även

* class [HtmlFixedSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* hopsättning [Aspose.Words](../../../)


