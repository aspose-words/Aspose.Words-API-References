---
title: FieldPrint.PostScriptGroup
linktitle: PostScriptGroup
articleTitle: PostScriptGroup
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FieldPrint PostScriptGroup för att enkelt hantera din ritningsrektangel för effektiv hantering av PostScript-instruktioner.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fieldprint/postscriptgroup/
---
## FieldPrint.PostScriptGroup property

Hämtar eller ställer in ritningsrektangeln som PostScript-instruktionerna fungerar på.

```csharp
public string PostScriptGroup { get; set; }
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
