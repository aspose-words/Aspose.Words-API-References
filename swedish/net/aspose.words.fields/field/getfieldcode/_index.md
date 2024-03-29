---
title: Field.GetFieldCode
linktitle: GetFieldCode
articleTitle: GetFieldCode
second_title: Aspose.Words för .NET
description: Field GetFieldCode metod. Returnerar text mellan fältstart och fältavgränsare eller fältslut om det inte finns någon avgränsare. Både fältkod och fältresultat för underordnade fält ingår i C#.
type: docs
weight: 110
url: /sv/net/aspose.words.fields/field/getfieldcode/
---
## GetFieldCode() {#getfieldcode}

Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). Både fältkod och fältresultat för underordnade fält ingår.

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
Assert.That(DateTime.Parse(field.Result), Is.EqualTo(DateTime.Today).Within(1).Days);
```

Visar hur man får ett fälts fältkod.

```csharp
// Öppna ett dokument som innehåller ett MERGEFIELD i ett IF-fält.
Document doc = new Document(MyDir + "Nested fields.docx");
FieldIf fieldIf = (FieldIf)doc.Range.Fields[0];

// Det finns två sätt att få ett fälts fältkod:
// 1 - Utelämna dess inre fält:
Assert.AreEqual(" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf.GetFieldCode(false));

// 2 - Inkludera dess inre fält:
Assert.AreEqual($" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" ",
    fieldIf.GetFieldCode(true));

// Som standard visar metoden GetFieldCode inre fält.
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
| includeChildFieldCodes | Boolean | `Sann` om underordnade fältkoder ska inkluderas. |

## Exempel

Visar hur man får ett fälts fältkod.

```csharp
// Öppna ett dokument som innehåller ett MERGEFIELD i ett IF-fält.
Document doc = new Document(MyDir + "Nested fields.docx");
FieldIf fieldIf = (FieldIf)doc.Range.Fields[0];

// Det finns två sätt att få ett fälts fältkod:
// 1 - Utelämna dess inre fält:
Assert.AreEqual(" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf.GetFieldCode(false));

// 2 - Inkludera dess inre fält:
Assert.AreEqual($" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" ",
    fieldIf.GetFieldCode(true));

// Som standard visar metoden GetFieldCode inre fält.
Assert.AreEqual(fieldIf.GetFieldCode(), fieldIf.GetFieldCode(true));
```

### Se även

* class [Field](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
