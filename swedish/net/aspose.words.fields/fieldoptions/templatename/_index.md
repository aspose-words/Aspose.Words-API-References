---
title: FieldOptions.TemplateName
second_title: Aspose.Words för .NET API Referens
description: FieldOptions fast egendom. Hämtar eller ställer in filnamnet på mallen som används av dokumentet.
type: docs
weight: 190
url: /sv/net/aspose.words.fields/fieldoptions/templatename/
---
## FieldOptions.TemplateName property

Hämtar eller ställer in filnamnet på mallen som används av dokumentet.

```csharp
public string TemplateName { get; set; }
```

### Anmärkningar

Den här egenskapen används av[`FieldTemplate`](../../fieldtemplate/) fältet om[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) fastigheten är tom.

Om den här egenskapen är tom, standard mallfilnamn`Normal.dotm` är använd.

### Exempel

Visar hur man använder ett MALL-fält för att visa den lokala filsystemets plats för ett dokuments mall.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Vi kan ställa in ett mallnamn med hjälp av fälten. Den här egenskapen används när "doc.AttachedTemplate" är tom.
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
* namnutrymme [Aspose.Words.Fields](../../fieldoptions/)
* hopsättning [Aspose.Words](../../../)


