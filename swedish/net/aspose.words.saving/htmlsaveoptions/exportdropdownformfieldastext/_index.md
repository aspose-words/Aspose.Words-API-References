---
title: HtmlSaveOptions.ExportDropDownFormFieldAsText
linktitle: ExportDropDownFormFieldAsText
articleTitle: ExportDropDownFormFieldAsText
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen HtmlSaveOptions ExportDropDownFormFieldAsText förbättrar dina HTML/MHTML-exporter genom att styra formaten för rullgardinsmenyer. Optimera dina dokument!
type: docs
weight: 130
url: /sv/net/aspose.words.saving/htmlsaveoptions/exportdropdownformfieldastext/
---
## HtmlSaveOptions.ExportDropDownFormFieldAsText property

Styr hur rullgardinsmenyfält sparas i HTML eller MHTML. Standardvärdet är`falsk` .

```csharp
public bool ExportDropDownFormFieldAsText { get; set; }
```

## Anmärkningar

När den är inställd på`sann` , exporterar rullgardinsmenyfält som vanlig text. När`falsk`, exporterar rullgardinsmenyfält som SELECT-element i HTML.

Vid export till EPUB sparas textfält i listrutorna alltid som text på grund av kraven i detta format.

## Exempel

Visar hur man får formulärfält i rullgardinsmenyer att blandas med stycketexten när man sparar till html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Använd en dokumentbyggare för att infoga en kombinationsruta med värdet "Två" valt.
builder.InsertComboBox("MyComboBox", new[] { "One", "Two", "Three" }, 1);

// Flaggan "ExportDropDownFormFieldAsText" för detta SaveOptions-objekt låter oss
// styr hur sparade dokument till HTML hanterar rullgardinsmenyer.
// Om du ställer in den på "true" konverteras varje kombinationsruta till enkel text
// som visar kombinationsrutans för närvarande valda värde, vilket i praktiken fryser det.
// Om du ställer in den på "false" bevaras funktionaliteten i kombinationsrutan med hjälp av taggarna <select> och <option>.
HtmlSaveOptions options = new HtmlSaveOptions();
options.ExportDropDownFormFieldAsText = exportDropDownFormFieldAsText;    

doc.Save(ArtifactsDir + "HtmlSaveOptions.DropDownFormField.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.DropDownFormField.html");

if (exportDropDownFormFieldAsText)
    Assert.True(outDocContents.Contains(
        "<span>Two</span>"));
else
    Assert.True(outDocContents.Contains(
        "<select name=\"MyComboBox\">" +
            "<option>One</option>" +
            "<option selected=\"selected\">Two</option>" +
            "<option>Three</option>" +
        "</select>"));
```

### Se även

* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
