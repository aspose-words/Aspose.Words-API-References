---
title: DocumentBuilder.Bold
linktitle: Bold
second_title: Aspose.Words for .NET API Reference
description: DocumentBuilder Bold property. True if the font is formatted as bold in C#.
type: docs
weight: 20
url: /net/aspose.words/documentbuilder/bold/
---
## DocumentBuilder.Bold property

True if the font is formatted as bold.

```csharp
public bool Bold { get; set; }
```

## Examples

Shows how to fill MERGEFIELDs with data with a document builder instead of a mail merge.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert some MERGEFIELDS, which accept data from columns of the same name in a data source during a mail merge,
// and then fill them manually.
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

### See Also

* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../documentbuilder/)
* assembly [Aspose.Words](../../../)
