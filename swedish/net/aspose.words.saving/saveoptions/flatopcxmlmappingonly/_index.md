---
title: SaveOptions.FlatOpcXmlMappingOnly
second_title: Aspose.Words för .NET API Referens
description: SaveOptions fast egendom. Hämtar eller ställer in värde som avgör vilka dokumentformat som tillåts mappas avXmlMapping . Endast som standardFlatOpc dokumentformat får mappas.
type: docs
weight: 90
url: /sv/net/aspose.words.saving/saveoptions/flatopcxmlmappingonly/
---
## SaveOptions.FlatOpcXmlMappingOnly property

Hämtar eller ställer in värde som avgör vilka dokumentformat som tillåts mappas av[`XmlMapping`](../../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Endast som standardFlatOpc dokumentformat får mappas.

```csharp
public bool FlatOpcXmlMappingOnly { get; set; }
```

### Anmärkningar

Det här alternativet är ihopparat med[`FlatOpcXmlMappingOnly`](../../../aspose.words.loading/loadoptions/flatopcxmlmappingonly/) . Vanligtvis måste du ställa in båda till false för att tillåta godtyckliga dokumentformat mappad.

### Exempel

Visar hur man binder strukturerade dokumenttaggar till valfritt format.

```csharp
// Om sant - SDT kommer att innehålla rå HTML-text.
// Om false - mappad HTML kommer att tolkas och resulterande dokument kommer att infogas i SDT-innehåll.
LoadOptions loadOptions = new LoadOptions { FlatOpcXmlMappingOnly = isFlatOpcXmlMappingOnly };
Document doc = new Document(MyDir + "Structured document tag with HTML content.docx", loadOptions);

SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Pdf);
saveOptions.FlatOpcXmlMappingOnly = isFlatOpcXmlMappingOnly;

doc.Save(ArtifactsDir + "LoadOptions.FlatOpcXmlMappingOnly.pdf", saveOptions);
```

### Se även

* class [SaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../saveoptions/)
* hopsättning [Aspose.Words](../../../)


