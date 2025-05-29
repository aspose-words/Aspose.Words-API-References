---
title: Field.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words för .NET
description: Upptäck fälttypen i Microsoft Word med vår Fälttyp-egenskap. Förbättra dina dokument med exakt formatering och dynamiska innehållsfunktioner.
type: docs
weight: 100
url: /sv/net/aspose.words.fields/field/type/
---
## Field.Type property

Hämtar fälttypen Microsoft Word.

```csharp
public virtual FieldType Type { get; }
```

## Exempel

Visar hur man infogar ett fält i ett dokument med hjälp av en fältkod.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Denna överbelastning av InsertField-metoden uppdaterar automatiskt infogade fält.
Assert.True((DateTime.Today - DateTime.Parse(field.Result)).Days <= 1);
```

### Se även

* enum [FieldType](../../fieldtype/)
* class [Field](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
