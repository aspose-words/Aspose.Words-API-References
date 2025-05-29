---
title: Field.Result
linktitle: Result
articleTitle: Result
second_title: Aspose.Words för .NET
description: Hantera fältresultategenskaper utan ansträngning. Få åtkomst till eller ändra text mellan fältavgränsare för effektiv datahantering och ökad effektivitet.
type: docs
weight: 70
url: /sv/net/aspose.words.fields/field/result/
---
## Field.Result property

Hämtar eller anger text som är mellan fältavgränsaren och fältslutet.

```csharp
public string Result { get; set; }
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

* class [Field](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
