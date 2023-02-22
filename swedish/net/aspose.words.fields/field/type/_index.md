---
title: Field.Type
second_title: Aspose.Words för .NET API Referens
description: Field fast egendom. Hämtar fälttypen Microsoft Word.
type: docs
weight: 100
url: /sv/net/aspose.words.fields/field/type/
---
## Field.Type property

Hämtar fälttypen Microsoft Word.

```csharp
public virtual FieldType Type { get; }
```

### Exempel

Visar hur man infogar ett fält i ett dokument med hjälp av en fältkod.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Denna överbelastning av InsertField-metoden uppdaterar automatiskt infogade fält.
Assert.That(DateTime.Parse(field.Result), Is.EqualTo(DateTime.Today).Within(1).Days);
```

### Se även

* enum [FieldType](../../fieldtype/)
* class [Field](../)
* namnutrymme [Aspose.Words.Fields](../../field/)
* hopsättning [Aspose.Words](../../../)


