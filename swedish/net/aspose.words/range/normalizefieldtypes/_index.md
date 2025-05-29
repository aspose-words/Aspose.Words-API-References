---
title: Range.NormalizeFieldTypes
linktitle: NormalizeFieldTypes
articleTitle: NormalizeFieldTypes
second_title: Aspose.Words för .NET
description: Transformera fälttyper med metoden NormalizeFieldTypes. Se till att FieldStart, FieldSeparator och FieldEnd är anpassade till angivna fältkoder för sömlös datahantering.
type: docs
weight: 90
url: /sv/net/aspose.words/range/normalizefieldtypes/
---
## Range.NormalizeFieldTypes method

Ändrar fälttypvärden[`FieldType`](../../../aspose.words.fields/fieldchar/fieldtype/) av[`FieldStart`](../../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../../aspose.words.fields/fieldend/) i detta intervall så att de motsvarar fälttyperna som finns i fältkoderna.

```csharp
public void NormalizeFieldTypes()
```

## Anmärkningar

Använd den här metoden efter dokumentändringar som påverkar fälttyper.

För att ändra fälttypvärden i hela dokumentet, använd[`NormalizeFieldTypes`](../../document/normalizefieldtypes/).

## Exempel

Visar hur man håller ett fälts typ uppdaterad med dess fältkod.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE", null);

// Aspose.Words detekterar automatiskt fälttyper baserat på fältkoder.
Assert.AreEqual(FieldType.FieldDate, field.Type);

// Ändra manuellt fältets råtext, vilket avgör fältkoden.
Run fieldText = (Run)doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Run, true)[0];
fieldText.Text = "PAGE";

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

* class [Range](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
