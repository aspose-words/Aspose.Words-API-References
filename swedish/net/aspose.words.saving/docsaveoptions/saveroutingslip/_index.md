---
title: DocSaveOptions.SaveRoutingSlip
second_title: Aspose.Words för .NET API Referens
description: DocSaveOptions fast egendom. Närfalsk  RoutingSlipdata sparas inte i utdatadokumentet. Standardvärdet är Sann .
type: docs
weight: 60
url: /sv/net/aspose.words.saving/docsaveoptions/saveroutingslip/
---
## DocSaveOptions.SaveRoutingSlip property

När`falsk` , RoutingSlip-data sparas inte i utdatadokumentet. Standardvärdet är **Sann** .

```csharp
public bool SaveRoutingSlip { get; set; }
```

### Exempel

Visar hur du ställer in sparalternativ för äldre Microsoft Word-format.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

DocSaveOptions options = new DocSaveOptions(SaveFormat.Doc);

// Ställ in ett lösenord som skyddar laddningen av dokumentet med Microsoft Word eller Aspose.Words.
// Observera att detta inte krypterar innehållet i dokumentet på något sätt.
options.Password = "MyPassword";

// Om dokumentet innehåller en routingsedel kan vi bevara den medan vi sparar genom att sätta denna flagga till true.
options.SaveRoutingSlip = true;

doc.Save(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", options);

// För att kunna ladda dokumentet,
// vi kommer att behöva använda lösenordet vi angav i DocSaveOptions-objektet i ett LoadOptions-objekt.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc"));

LoadOptions loadOptions = new LoadOptions("MyPassword");
doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", loadOptions);

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Se även

* class [DocSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../docsaveoptions/)
* hopsättning [Aspose.Words](../../../)


