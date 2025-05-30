---
title: ImportFormatOptions.MergePastedLists
linktitle: MergePastedLists
articleTitle: MergePastedLists
second_title: Aspose.Words för .NET
description: Kontrolllistor som slås samman med egenskapen ImportFormatOptions MergePastedLists. Hantera enkelt inklistrade listor för att förbättra dokumentformateringen. Standardvärde falskt.
type: docs
weight: 70
url: /sv/net/aspose.words/importformatoptions/mergepastedlists/
---
## ImportFormatOptions.MergePastedLists property

Hämtar eller ställer in ett booleskt värde som anger om inklistrade listor ska slås samman med omgivande listor. Standardvärdet är`falsk` .

```csharp
public bool MergePastedLists { get; set; }
```

## Exempel

Visar hur man sammanfogar listor från dokument.

```csharp
Document srcDoc = new Document(MyDir + "List item.docx");
Document dstDoc = new Document(MyDir + "List destination.docx");

ImportFormatOptions options = new ImportFormatOptions { MergePastedLists = true };

// Sätt egenskapen "MergePastedLists" till "true" så kommer inklistrade listor att slås samman med omgivande listor.
dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, options);

dstDoc.Save(ArtifactsDir + "Document.MergePastedLists.docx");
```

### Se även

* class [ImportFormatOptions](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
