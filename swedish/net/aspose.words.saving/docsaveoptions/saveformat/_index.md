---
title: DocSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words för .NET
description: Upptäck egenskapen DocSaveOptions SaveFormat för att enkelt välja mellan Doc- eller Dot-format för sömlös dokumentsparning. Optimera ditt arbetsflöde idag!
type: docs
weight: 50
url: /sv/net/aspose.words.saving/docsaveoptions/saveformat/
---
## DocSaveOptions.SaveFormat property

Anger formatet som dokumentet sparas i om detta objekt för sparade alternativ används. Kan varaDoc ellerDot .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Exempel

Visar hur man ställer in sparalternativ för äldre Microsoft Word-format.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

DocSaveOptions options = new DocSaveOptions(SaveFormat.Doc);

// Ange ett lösenord som skyddar inläsningen av dokumentet med Microsoft Word eller Aspose.Words.
// Observera att detta inte krypterar dokumentets innehåll på något sätt.
options.Password = "MyPassword";

// Om dokumentet innehåller en rutningsbekräftelse kan vi bevara den medan vi sparar genom att sätta denna flagga till true.
options.SaveRoutingSlip = true;

doc.Save(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", options);

// För att kunna ladda dokumentet,
// vi måste använda lösenordet som vi angav i DocSaveOptions-objektet i ett LoadOptions-objekt.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc"));

LoadOptions loadOptions = new LoadOptions("MyPassword");
doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", loadOptions);

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Se även

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [DocSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
