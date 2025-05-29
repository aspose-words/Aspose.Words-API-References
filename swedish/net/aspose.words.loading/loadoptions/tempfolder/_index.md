---
title: LoadOptions.TempFolder
linktitle: TempFolder
articleTitle: TempFolder
second_title: Aspose.Words för .NET
description: Optimera dokumentläsning med LoadOptions TempFolder-egenskap. Hantera enkelt temporära filer för effektiv bearbetning och förbättrad prestanda.
type: docs
weight: 150
url: /sv/net/aspose.words.loading/loadoptions/tempfolder/
---
## LoadOptions.TempFolder property

Tillåter användning av temporära filer vid läsning av dokument. Som standard är den här egenskapen`null` och inga temporära filer används.

```csharp
public string TempFolder { get; set; }
```

## Anmärkningar

Mappen måste finnas och vara skrivbar, annars kommer ett undantag att utlösas.

Aspose.Words tar automatiskt bort alla temporära filer när läsningen är klar.

## Exempel

Visar hur man laddar ett dokument med hjälp av temporära filer.

```csharp
// Observera att en sådan metod kan minska minnesanvändningen men försämra hastigheten
LoadOptions loadOptions = new LoadOptions();
loadOptions.TempFolder = @"C:\TempFolder\";

// Se till att katalogen finns och ladda
Directory.CreateDirectory(loadOptions.TempFolder);

Document doc = new Document(MyDir + "Document.docx", loadOptions);
```

Visar hur man använder hårddisken istället för minne när man laddar ett dokument.

```csharp
// När vi laddar ett dokument lagras olika element tillfälligt i minnet medan sparoperationen sker.
// Vi kan använda det här alternativet för att istället använda en tillfällig mapp i det lokala filsystemet,
// vilket kommer att minska vår applikations minnesbelastning.
LoadOptions options = new LoadOptions();
options.TempFolder = ArtifactsDir + "TempFiles";

// Den angivna temporära mappen måste finnas i det lokala filsystemet innan laddningsoperationen.
Directory.CreateDirectory(options.TempFolder);

Document doc = new Document(MyDir + "Document.docx", options);

// Mappen kommer att finnas kvar utan kvarvarande innehåll från laddningsoperationen.
Assert.AreEqual(0, Directory.GetFiles(options.TempFolder).Length);
```

### Se även

* class [LoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../../)
