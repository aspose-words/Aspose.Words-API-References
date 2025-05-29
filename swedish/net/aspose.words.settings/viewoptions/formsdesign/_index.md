---
title: ViewOptions.FormsDesign
linktitle: FormsDesign
articleTitle: FormsDesign
second_title: Aspose.Words för .NET
description: Upptäck hur ViewOptions FormsDesign förbättrar din dokumentupplevelse genom att aktivera och växla formulärdesignläge för sömlös redigering och anpassning.
type: docs
weight: 30
url: /sv/net/aspose.words.settings/viewoptions/formsdesign/
---
## ViewOptions.FormsDesign property

Anger om dokumentet är i formulärdesignläge.

```csharp
public bool FormsDesign { get; set; }
```

## Anmärkningar

Fungerar för närvarande endast för dokument i WordML-format.

## Exempel

Visar hur man aktiverar/inaktiverar formulärdesignläge.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Sätt egenskapen "FormsDesign" till "false" för att hålla formulärdesignläget inaktiverat.
// Sätt egenskapen "FormsDesign" till "true" för att aktivera formulärdesignläge.
doc.ViewOptions.FormsDesign = useFormsDesign;

doc.Save(ArtifactsDir + "ViewOptions.FormsDesign.xml");

Assert.AreEqual(useFormsDesign,
    File.ReadAllText(ArtifactsDir + "ViewOptions.FormsDesign.xml").Contains("<w:formsDesign />"));
```

### Se även

* class [ViewOptions](../)
* namnutrymme [Aspose.Words.Settings](../../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../../)
