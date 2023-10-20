---
title: ImportFormatOptions.MergePastedLists
linktitle: MergePastedLists
articleTitle: MergePastedLists
second_title: Aspose.Words för .NET
description: ImportFormatOptions MergePastedLists fast egendom. Hämtar eller ställer in ett booleskt värde som anger om inklistrade listor ska slås samman med omgivande listor. Standardvärdet ärfalsk  i C#.
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

Visar hur man slår samman listor från ett dokument.

```csharp
Document srcDoc = new Document(MyDir + "List item.docx");
Document dstDoc = new Document(MyDir + "List destination.docx");

ImportFormatOptions options = new ImportFormatOptions { MergePastedLists = true };

// Ställ in egenskapen "MergePastedLists" till "true" inklistrade listor kommer att slås samman med omgivande listor.
dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, options);

dstDoc.Save(ArtifactsDir + "Document.MergePastedLists.docx");
```

### Se även

* class [ImportFormatOptions](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
