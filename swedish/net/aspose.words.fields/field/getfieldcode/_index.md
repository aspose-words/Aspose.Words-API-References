---
title: Field.GetFieldCode
linktitle: GetFieldCode
articleTitle: GetFieldCode
second_title: Aspose.Words för .NET
description: Upptäck GetFieldCode-metoden, hämta enkelt text mellan fältstart och avgränsare, inklusive underfältkoder och resultat. Öka din kodningseffektivitet!
type: docs
weight: 110
url: /sv/net/aspose.words.fields/field/getfieldcode/
---
## GetFieldCode() {#getfieldcode}

Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). Både fältkod och fältresultat för underfält inkluderas.

```csharp
public string GetFieldCode()
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

Visar hur man hämtar ett fälts fältkod.

```csharp
// Öppna ett dokument som innehåller ett MERGEFIELD inuti ett OM-fält.
Document doc = new Document(MyDir + "Nested fields.docx");
FieldIf fieldIf = (FieldIf)doc.Range.Fields[0];

// Det finns två sätt att hämta ett fälts fältkod:
// 1 - Utelämna dess inre fält:
Assert.AreEqual(" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf.GetFieldCode(false));

// 2 - Inkludera dess inre fält:
Assert.AreEqual($" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" ",
    fieldIf.GetFieldCode(true));

// Som standard visar GetFieldCode-metoden inre fält.
Assert.AreEqual(fieldIf.GetFieldCode(), fieldIf.GetFieldCode(true));
```

### Se även

* class [Field](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)

---

## GetFieldCode(*bool*) {#getfieldcode_1}

Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare).

```csharp
public string GetFieldCode(bool includeChildFieldCodes)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| includeChildFieldCodes | Boolean | `sann` om underordnade fältkoder ska inkluderas. |

## Exempel

Visar hur man hämtar ett fälts fältkod.

```csharp
// Öppna ett dokument som innehåller ett MERGEFIELD inuti ett OM-fält.
Document doc = new Document(MyDir + "Nested fields.docx");
FieldIf fieldIf = (FieldIf)doc.Range.Fields[0];

// Det finns två sätt att hämta ett fälts fältkod:
// 1 - Utelämna dess inre fält:
Assert.AreEqual(" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf.GetFieldCode(false));

// 2 - Inkludera dess inre fält:
Assert.AreEqual($" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" ",
    fieldIf.GetFieldCode(true));

// Som standard visar GetFieldCode-metoden inre fält.
Assert.AreEqual(fieldIf.GetFieldCode(), fieldIf.GetFieldCode(true));
```

### Se även

* class [Field](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
