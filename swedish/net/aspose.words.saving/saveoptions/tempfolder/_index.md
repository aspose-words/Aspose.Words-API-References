---
title: SaveOptions.TempFolder
linktitle: TempFolder
articleTitle: TempFolder
second_title: Aspose.Words för .NET
description: Optimera din dokumentsparning med egenskapen SaveOptions TempFolder, som anger en mapp för tillfälliga DOC- och DOCX-filer, vilket förbättrar effektiviteten.
type: docs
weight: 140
url: /sv/net/aspose.words.saving/saveoptions/tempfolder/
---
## SaveOptions.TempFolder property

Anger mappen för temporära filer som används när man sparar till en DOC- eller DOCX-fil. Som standard är den här egenskapen`null` och inga temporära filer används.

```csharp
public string TempFolder { get; set; }
```

### Undantag

| undantag | skick |
| --- | --- |
| OutOfMemoryException | Kasta om du sparar ett mycket stort dokument (tusentals sidor) och/eller bearbetar många dokument samtidigt. Minnesstoppen under sparandet kan vara tillräckligt betydande för att orsaka undantaget. |

## Anmärkningar

När Aspose.Words sparar ett dokument måste det skapa tillfälliga interna strukturer. Som standard skapas dessa interna strukturer i minnet och minnesanvändningen ökar kraftigt under en kort period medan dokumentet sparas. När sparandet är klart frigörs minnet och återanvänds av skräpinsamlaren.

Ange en tillfällig mapp med hjälp av`TempFolder` kommer att få Aspose.Words att behålla de interna strukturerna i temporära filer i istället för minne. Det minskar minnesanvändningen under sparande, men kommer att minska prestandan vid sparning.

Mappen måste finnas och vara skrivbar, annars kommer ett undantag att utlösas.

Aspose.Words tar automatiskt bort alla temporära filer när sparandet är klart.

## Exempel

Visar hur man använder hårddisken istället för minne när man sparar ett dokument.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// När vi sparar ett dokument lagras olika element tillfälligt i minnet medan sparoperationen pågår.
// Vi kan använda det här alternativet för att istället använda en tillfällig mapp i det lokala filsystemet,
// vilket kommer att minska vår applikations minnesbelastning.
DocSaveOptions options = new DocSaveOptions();
options.TempFolder = ArtifactsDir + "TempFiles";

// Den angivna temporära mappen måste finnas i det lokala filsystemet innan sparoperationen.
Directory.CreateDirectory(options.TempFolder);

doc.Save(ArtifactsDir + "DocSaveOptions.TempFolder.doc", options);

// Mappen kommer att finnas kvar utan kvarvarande innehåll från laddningsoperationen.
Assert.AreEqual(0, Directory.GetFiles(options.TempFolder).Length);
```

### Se även

* class [SaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
