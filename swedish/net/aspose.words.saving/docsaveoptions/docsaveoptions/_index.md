---
title: DocSaveOptions
linktitle: DocSaveOptions
articleTitle: DocSaveOptions
second_title: Aspose.Words för .NET
description: Upptäck konstruktorn DocSaveOptions för sömlös dokumentsparning i Doc-format. Förbättra ditt arbetsflöde med enkel och effektiv dokumenthantering.
type: docs
weight: 10
url: /sv/net/aspose.words.saving/docsaveoptions/docsaveoptions/
---
## DocSaveOptions() {#constructor}

Initierar en ny instans av den här klassen som kan användas för att spara ett dokument iDoc format.

```csharp
public DocSaveOptions()
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

---

## DocSaveOptions(*[SaveFormat](../../../aspose.words/saveformat/)*) {#constructor_1}

Initierar en ny instans av den här klassen som kan användas för att spara ett dokument iDoc eller Dot format.

```csharp
public DocSaveOptions(SaveFormat saveFormat)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| saveFormat | SaveFormat | Kan varaDoc ellerDot. |

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
