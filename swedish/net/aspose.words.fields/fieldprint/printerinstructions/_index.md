---
title: FieldPrint.PrinterInstructions
linktitle: PrinterInstructions
articleTitle: PrinterInstructions
second_title: Aspose.Words för .NET
description: Upptäck hur du hanterar skrivarspecifika kontrollkoder och PostScript-instruktioner med FieldPrint PrinterInstructions för optimerade utskriftslösningar.
type: docs
weight: 30
url: /sv/net/aspose.words.fields/fieldprint/printerinstructions/
---
## FieldPrint.PrinterInstructions property

Hämtar eller ställer in skrivarspecifika kontrollkodstecken eller PostScript-instruktioner.

```csharp
public string PrinterInstructions { get; set; }
```

## Exempel

Visar för att infoga ett PRINT-fält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("My paragraph");

// Fältet PRINT kan skicka instruktioner till skrivaren.
FieldPrint field = (FieldPrint)builder.InsertField(FieldType.FieldPrint, true);

// Ange området där skrivaren ska utföra instruktioner.
// I det här fallet kommer det att vara stycket som innehåller vårt PRINT-fält.
field.PostScriptGroup = "para";

// När vi använder en skrivare som stöder PostScript för att skriva ut vårt dokument,
// det här kommandot kommer att göra hela området som vi angav i "field.PostScriptGroup" vitt.
field.PrinterInstructions = "erasepage";

Assert.AreEqual(" PRINT  erasepage \\p para", field.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.PRINT.docx");
```

### Se även

* class [FieldPrint](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
