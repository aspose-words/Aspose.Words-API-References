---
title: LoadOptions.TempFolder
second_title: Aspose.Words för .NET API Referens
description: LoadOptions fast egendom. Tillåter att använda temporära filer vid läsning av dokument. Som standard är denna egenskapnull och inga temporära filer används.
type: docs
weight: 150
url: /sv/net/aspose.words.loading/loadoptions/tempfolder/
---
## LoadOptions.TempFolder property

Tillåter att använda temporära filer vid läsning av dokument. Som standard är denna egenskap`null` och inga temporära filer används.

```csharp
public string TempFolder { get; set; }
```

### Anmärkningar

Mappen måste finnas och vara skrivbar, annars kommer ett undantag att kastas.

Aspose.Words tar automatiskt bort alla temporära filer när läsningen är klar.

### Exempel

Visar hur man laddar ett dokument med hjälp av temporära filer.

```csharp
// Observera att ett sådant tillvägagångssätt kan minska minnesanvändningen men minskar hastigheten
LoadOptions loadOptions = new LoadOptions();
loadOptions.TempFolder = @"C:\TempFolder\";

// Se till att katalogen finns och ladda
Directory.CreateDirectory(loadOptions.TempFolder);

Document doc = new Document(MyDir + "Document.docx", loadOptions);
```

Visar hur du använder hårddisken istället för minnet när du laddar ett dokument.

```csharp
// När vi laddar ett dokument lagras olika element tillfälligt i minnet när lagringen sker.
// Vi kan använda det här alternativet för att använda en tillfällig mapp i det lokala filsystemet istället,
// som kommer att minska vår applikations minnesoverhead.
LoadOptions options = new LoadOptions();
options.TempFolder = ArtifactsDir + "TempFiles";

// Den angivna temporära mappen måste finnas i det lokala filsystemet innan laddningsoperationen.
Directory.CreateDirectory(options.TempFolder);

Document doc = new Document(MyDir + "Document.docx", options);

// Mappen kommer att finnas kvar utan kvarvarande innehåll från laddningsoperationen.
Assert.That(Directory.GetFiles(options.TempFolder), Is.Empty);
```

### Se även

* class [LoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../loadoptions/)
* hopsättning [Aspose.Words](../../../)


