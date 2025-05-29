---
title: FieldOptions.TemplateName
linktitle: TemplateName
articleTitle: TemplateName
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FieldOptions TemplateName för att enkelt hantera dokumentets mallfilnamn för förbättrad organisation och effektivitet.
type: docs
weight: 190
url: /sv/net/aspose.words.fields/fieldoptions/templatename/
---
## FieldOptions.TemplateName property

Hämtar eller anger filnamnet på mallen som används av dokumentet.

```csharp
public string TemplateName { get; set; }
```

## Anmärkningar

Denna egenskap används av[`FieldTemplate`](../../fieldtemplate/) fältet om[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) fastigheten är tom.

Om den här egenskapen är tom, standardmallens filnamn`Normal.dotm` används.

## Exempel

Visar hur man använder ett MALL-fält för att visa den lokala filsystemets plats för en dokumentmall.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Vi kan ange ett mallnamn med hjälp av fälten. Den här egenskapen används när "doc.AttachedTemplate" är tom.
// Om den här egenskapen är tom används standardmallfilnamnet "Normal.dotm".
doc.FieldOptions.TemplateName = string.Empty;

FieldTemplate field = (FieldTemplate)builder.InsertField(FieldType.FieldTemplate, false);
Assert.AreEqual(" TEMPLATE ", field.GetFieldCode());

builder.Writeln();
field = (FieldTemplate)builder.InsertField(FieldType.FieldTemplate, false);
field.IncludeFullPath = true;

Assert.AreEqual(" TEMPLATE  \\p", field.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.TEMPLATE.docx");
```

### Se även

* class [FieldOptions](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
