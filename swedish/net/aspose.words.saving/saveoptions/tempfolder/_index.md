---
title: SaveOptions.TempFolder
linktitle: TempFolder
articleTitle: TempFolder
second_title: Aspose.Words för .NET
description: SaveOptions TempFolder fast egendom. Anger mappen för temporära filer som används när du sparar till en DOC eller DOCXfil. Som standard är denna egenskapnull och inga temporära filer används i C#.
type: docs
weight: 140
url: /sv/net/aspose.words.saving/saveoptions/tempfolder/
---
## SaveOptions.TempFolder property

Anger mappen för temporära filer som används när du sparar till en DOC- eller DOCX-fil. Som standard är denna egenskap`null` och inga temporära filer används.

```csharp
public string TempFolder { get; set; }
```

## Anmärkningar

När Aspose.Words sparar ett dokument måste det skapa tillfälliga interna strukturer. Som standard skapas dessa interna strukturer i minnet och minnesanvändningen ökar under en kort period medan dokumentet sparas. När lagringen är klar frigörs minnet och återvinns av sopsamlaren.

Om du sparar ett mycket stort dokument (tusentals sidor) och/eller bearbetar många dokument samtidigt, kan minneshöjningen under sparandet vara tillräckligt stor för att få systemet att kastaOutOfMemoryException . Ange en tillfällig mapp med hjälp av`TempFolder` kommer att få Aspose.Words att behålla de interna strukturerna i temporära filer istället för minne. Det minskar minnesanvändningen under lagring, men kommer att minska lagringsprestanda.

Mappen måste finnas och vara skrivbar, annars kommer ett undantag att kastas.

Aspose.Words tar automatiskt bort alla temporära filer när sparandet är klart.

## Exempel

Visar hur du använder hårddisken istället för minnet när du sparar ett dokument.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// När vi sparar ett dokument, lagras olika element tillfälligt i minnet när lagringsoperationen pågår.
// Vi kan använda det här alternativet för att använda en tillfällig mapp i det lokala filsystemet istället,
// som kommer att minska vår applikations minnesoverhead.
DocSaveOptions options = new DocSaveOptions();
options.TempFolder = ArtifactsDir + "TempFiles";

// Den angivna temporära mappen måste finnas i det lokala filsystemet innan du sparar.
Directory.CreateDirectory(options.TempFolder);

doc.Save(ArtifactsDir + "DocSaveOptions.TempFolder.doc", options);

// Mappen kommer att finnas kvar utan kvarvarande innehåll från laddningsoperationen.
Assert.That(Directory.GetFiles(options.TempFolder), Is.Empty);
```

### Se även

* class [SaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
