---
title: Document.NormalizeFieldTypes
second_title: Aspose.Words för .NET API Referens
description: Document metod. Ändrar fälttypvärdenFieldType avFieldStart FieldSeparator FieldEnd i hela dokumentet så att de motsvarar fälttyperna som finns i fältkoderna.
type: docs
weight: 610
url: /sv/net/aspose.words/document/normalizefieldtypes/
---
## Document.NormalizeFieldTypes method

Ändrar fälttypvärden[`FieldType`](../../../aspose.words.fields/fieldchar/fieldtype/) av[`FieldStart`](../../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../../aspose.words.fields/fieldend/) i hela dokumentet så att de motsvarar fälttyperna som finns i fältkoderna.

```csharp
public void NormalizeFieldTypes()
```

### Anmärkningar

Använd den här metoden efter dokumentändringar som påverkar fälttyper.

För att ändra fälttypvärden i en specifik del av dokumentet använd[`NormalizeFieldTypes`](../../range/normalizefieldtypes/).

### Exempel

Visar hur du håller ett fälts typ uppdaterad med dess fältkod.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE", null);

// Aspose.Words upptäcker automatiskt fälttyper baserat på fältkoder.
Assert.AreEqual(FieldType.FieldDate, field.Type);

// Ändra fältets råtext manuellt, vilket bestämmer fältkoden.
Run fieldText = (Run)doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Run, true)[0];

// Ändring av fältkoden har ändrat detta fält till ett av en annan typ,
// men fältets typegenskaper visar fortfarande den gamla typen.
Assert.AreEqual("PAGE", field.GetFieldCode());
Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual(FieldType.FieldDate, field.Start.FieldType);
Assert.AreEqual(FieldType.FieldDate, field.Separator.FieldType);
Assert.AreEqual(FieldType.FieldDate, field.End.FieldType);

// Uppdatera dessa egenskaper med den här metoden för att visa aktuellt värde.
doc.NormalizeFieldTypes();

Assert.AreEqual(FieldType.FieldPage, field.Type);
Assert.AreEqual(FieldType.FieldPage, field.Start.FieldType);
Assert.AreEqual(FieldType.FieldPage, field.Separator.FieldType); 
Assert.AreEqual(FieldType.FieldPage, field.End.FieldType);
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../document/)
* hopsättning [Aspose.Words](../../../)


