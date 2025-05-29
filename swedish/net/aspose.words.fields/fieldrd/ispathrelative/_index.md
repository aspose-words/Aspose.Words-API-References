---
title: FieldRD.IsPathRelative
linktitle: IsPathRelative
articleTitle: IsPathRelative
second_title: Aspose.Words för .NET
description: Upptäck FieldRDs IsPathRelative-egenskap för att enkelt hantera dokumentsökvägar. Förenkla din kodning med flexibla sökvägsinställningar för ökad effektivitet!
type: docs
weight: 30
url: /sv/net/aspose.words.fields/fieldrd/ispathrelative/
---
## FieldRD.IsPathRelative property

Hämtar eller anger om sökvägen är relativ till det aktuella dokumentet.

```csharp
public bool IsPathRelative { get; set; }
```

## Exempel

Visar hur man använder RD-fältet för att skapa innehållsförteckningsposter från rubriker i andra dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Använd en dokumentbyggare för att infoga en innehållsförteckning,
// och lägg sedan till en post för innehållsförteckningen på följande sida.
builder.InsertField(FieldType.FieldTOC, true);
builder.InsertBreak(BreakType.PageBreak);
builder.CurrentParagraph.ParagraphFormat.StyleName = "Heading 1";
builder.Writeln("TOC entry from within this document");

// Infoga ett RD-fält som refererar till ett annat lokalt filsystemdokument i dess FileName-egenskap.
// Innehållsförteckningen kommer nu också att acceptera alla rubriker från det refererade dokumentet som poster för sin tabell.
FieldRD field = (FieldRD)builder.InsertField(FieldType.FieldRefDoc, true);
field.FileName = ArtifactsDir + "ReferencedDocument.docx";

Assert.AreEqual($" RD  {ArtifactsDir.Replace(@"\",@"\\")}ReferencedDocument.docx", field.GetFieldCode());

 // Skapa dokumentet som RD-fältet refererar till och infoga en rubrik.
// Denna rubrik kommer att visas som en post i innehållsförteckningsfältet i vårt första dokument.
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
