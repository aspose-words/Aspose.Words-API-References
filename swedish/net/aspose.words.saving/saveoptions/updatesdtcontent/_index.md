---
title: SaveOptions.UpdateSdtContent
second_title: Aspose.Words för .NET API Referens
description: SaveOptions fast egendom. Hämtar eller ställer in värde som avgör om innehållet iStructuredDocumentTag uppdateras innan du sparar.
type: docs
weight: 200
url: /sv/net/aspose.words.saving/saveoptions/updatesdtcontent/
---
## SaveOptions.UpdateSdtContent property

Hämtar eller ställer in värde som avgör om innehållet i[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) uppdateras innan du sparar.

```csharp
public bool UpdateSdtContent { get; set; }
```

### Anmärkningar

Standardvärdet är`Sann` .

### Exempel

Visar hur du uppdaterar strukturerade dokumenttaggar samtidigt som du sparar ett dokument till PDF.

```csharp
Document doc = new Document();

// Infoga en strukturerad dokumenttagg i rullgardinsmenyn.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DropDownList, MarkupLevel.Block);
tag.ListItems.Add(new SdtListItem("Value 1"));
tag.ListItems.Add(new SdtListItem("Value 2"));
tag.ListItems.Add(new SdtListItem("Value 3"));

// Rullgardinslistan visar för närvarande "Välj ett objekt" som standardtext.
// Ställ in egenskapen "SelectedValue" till ett av listobjekten att hämta taggen till
// visa listobjektets värde istället för standardtexten.
tag.ListItems.SelectedValue = tag.ListItems[1];

doc.FirstSection.Body.AppendChild(tag);

// Skapa ett "PdfSaveOptions"-objekt för att skicka till dokumentets "Spara"-metod
// för att ändra hur den metoden sparar dokumentet till .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Ställ in egenskapen "UpdateSdtContent" till "false" för att inte uppdatera de strukturerade dokumenttaggarna
// medan du sparar dokumentet till PDF. De kommer att visa sina standardvärden som de var vid konstruktionstillfället.
// Ställ in egenskapen "UpdateSdtContent" till "true" för att se till att taggarna visar uppdaterade värden i PDF:en.
options.UpdateSdtContent = updateSdtContent;

doc.Save(ArtifactsDir + "StructuredDocumentTag.UpdateSdtContent.pdf", options);
```

### Se även

* class [SaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../saveoptions/)
* hopsättning [Aspose.Words](../../../)


