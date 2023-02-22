---
title: FieldTemplate.IncludeFullPath
second_title: Aspose.Words för .NET API Referens
description: FieldTemplate fast egendom. Hämtar eller ställer in om det fullständiga sökvägsnamnet ska inkluderas.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fieldtemplate/includefullpath/
---
## FieldTemplate.IncludeFullPath property

Hämtar eller ställer in om det fullständiga sökvägsnamnet ska inkluderas.

```csharp
public bool IncludeFullPath { get; set; }
```

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

* class [FieldTemplate](../)
* namnutrymme [Aspose.Words.Fields](../../fieldtemplate/)
* hopsättning [Aspose.Words](../../../)


