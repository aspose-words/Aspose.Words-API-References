---
title: DocumentBuilder.Italic
linktitle: Italic
articleTitle: Italic
second_title: Aspose.Words för .NET
description: Upptäck DocumentBuilder kursiv stil. Formatera enkelt din text i kursiv stil för förbättrad läsbarhet och stil i dina dokument.
type: docs
weight: 140
url: /sv/net/aspose.words/documentbuilder/italic/
---
## DocumentBuilder.Italic property

Sant om teckensnittet är formaterat som kursiv stil.

```csharp
public bool Italic { get; set; }
```

## Exempel

Visar hur man fyller MERGEFIELDs med data med en dokumentbyggare istället för en dokumentkoppling.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga några MERGEFIELDS, som accepterar data från kolumner med samma namn i en datakälla under en dokumentkoppling,
// och fyll sedan i dem manuellt.
builder.InsertField(" MERGEFIELD Chairman ");
builder.InsertField(" MERGEFIELD ChiefFinancialOfficer ");
builder.InsertField(" MERGEFIELD ChiefTechnologyOfficer ");

builder.MoveToMergeField("Chairman");
builder.Bold = true;
builder.Writeln("John Doe");

builder.MoveToMergeField("ChiefFinancialOfficer");
builder.Italic = true;
builder.Writeln("Jane Doe");

builder.MoveToMergeField("ChiefTechnologyOfficer");
builder.Italic = true;
builder.Writeln("John Bloggs");

doc.Save(ArtifactsDir + "DocumentBuilder.FillMergeFields.docx");
```

### Se även

* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
