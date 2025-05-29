---
title: DocSaveOptions.SaveRoutingSlip
linktitle: SaveRoutingSlip
articleTitle: SaveRoutingSlip
second_title: Aspose.Words för .NET
description: Upptäck egenskapen SaveRoutingSlip i DocSaveOptions. Kontrollera sparandet av RoutingSlip-data för dina dokument. Förbättra anpassningen av utdata enkelt!
type: docs
weight: 70
url: /sv/net/aspose.words.saving/docsaveoptions/saveroutingslip/
---
## DocSaveOptions.SaveRoutingSlip property

När`falsk` , RoutingSlip-data sparas inte i utdatadokumentet. Standardvärdet är`sann` .

```csharp
public bool SaveRoutingSlip { get; set; }
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

* class [DocSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
