---
title: DocumentBuilder.Bold
linktitle: Bold
articleTitle: Bold
second_title: Aspose.Words för .NET
description: Upptäck DocumentBuilder Bold-egenskapen. Formatera enkelt teckensnitt som fetstil för att förbättra textens synlighet och effekt i dina dokument. Förbättra din design idag!
type: docs
weight: 20
url: /sv/net/aspose.words/documentbuilder/bold/
---
## DocumentBuilder.Bold property

Sant om teckensnittet är formaterat som fetstil.

```csharp
public bool Bold { get; set; }
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
