---
title: FieldRD.FileName
linktitle: FileName
articleTitle: FileName
second_title: Aspose.Words för .NET
description: FieldRD FileName fast egendom. Hämtar eller ställer in namnet på filen som ska inkluderas när en innehållsförteckning behörighetsförteckning eller index genereras i C#.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fieldrd/filename/
---
## FieldRD.FileName property

Hämtar eller ställer in namnet på filen som ska inkluderas när en innehållsförteckning, behörighetsförteckning eller index genereras.

```csharp
public string FileName { get; set; }
```

## Exempel

Visar att använda RD-fältet för att skapa en innehållsförteckning från rubriker i andra dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Använd en dokumentbyggare för att infoga en innehållsförteckning,
// och lägg sedan till en post för innehållsförteckningen på följande sida.
builder.InsertField(FieldType.FieldTOC, true);
builder.InsertBreak(BreakType.PageBreak);
builder.CurrentParagraph.ParagraphFormat.StyleName = "Heading 1";
builder.Writeln("TOC entry from within this document");

// Infoga ett RD-fält, som refererar till ett annat lokalt filsystemdokument i dess FileName-egenskap.
// TOC kommer nu också att acceptera alla rubriker från det refererade dokumentet som poster för sin tabell.
FieldRD field = (FieldRD)builder.InsertField(FieldType.FieldRefDoc, true);
field.FileName = ArtifactsDir + "ReferencedDocument.docx";

Assert.AreEqual($" RD  {ArtifactsDir.Replace(@"\",@"\\")}ReferencedDocument.docx", field.GetFieldCode());

 // Skapa dokumentet som RD-fältet refererar till och infoga en rubrik.
// Den här rubriken kommer att dyka upp som en post i TOC-fältet i vårt första dokument.
Document referencedDoc = new Document();
DocumentBuilder refDocBuilder = new DocumentBuilder(referencedDoc);
refDocBuilder.CurrentParagraph.ParagraphFormat.StyleName = "Heading 1";
refDocBuilder.Writeln("TOC entry from referenced document");
referencedDoc.Save(ArtifactsDir + "ReferencedDocument.docx");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.RD.docx");
```

### Se även

* class [FieldRD](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
