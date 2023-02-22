---
title: Field.GetFieldCode
second_title: Aspose.Words für .NET-API-Referenz
description: Field methode. Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück oder Feldende wenn kein Trennzeichen vorhanden ist. Sowohl Feldcode als auch Feldergebnis von untergeordneten Feldern sind enthalten.
type: docs
weight: 110
url: /de/net/aspose.words.fields/field/getfieldcode/
---
## GetFieldCode() {#getfieldcode}

Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldergebnis von untergeordneten Feldern sind enthalten.

```csharp
public string GetFieldCode()
```

### Beispiele

Zeigt, wie ein Feld mithilfe eines Feldcodes in ein Dokument eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Diese Überladung der InsertField-Methode aktualisiert automatisch eingefügte Felder.
Assert.That(DateTime.Parse(field.Result), Is.EqualTo(DateTime.Today).Within(1).Days);
```

Zeigt, wie der Feldcode eines Felds abgerufen wird.

```csharp
// Öffne ein Dokument, das ein MERGEFIELD in einem IF-Feld enthält.
Document doc = new Document(MyDir + "Nested fields.docx");
FieldIf fieldIf = (FieldIf)doc.Range.Fields[0];

// Es gibt zwei Möglichkeiten, den Feldcode eines Felds zu erhalten:
// 1 - Lassen Sie die inneren Felder weg:
Assert.AreEqual(" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf.GetFieldCode(false));

// 2 - Fügen Sie die inneren Felder hinzu:
Assert.AreEqual($" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" ",
    fieldIf.GetFieldCode(true));

// Standardmäßig zeigt die GetFieldCode-Methode innere Felder an.
Assert.AreEqual(fieldIf.GetFieldCode(), fieldIf.GetFieldCode(true));
```

### Siehe auch

* class [Field](../)
* namensraum [Aspose.Words.Fields](../../field/)
* Montage [Aspose.Words](../../../)

---

## GetFieldCode(bool) {#getfieldcode_1}

Gibt Text zwischen Feldanfang und Feldtrennzeichen (oder Feldende, wenn kein Trennzeichen vorhanden ist) zurück.

```csharp
public string GetFieldCode(bool includeChildFieldCodes)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| includeChildFieldCodes | Boolean | `WAHR` ob untergeordnete Feldcodes enthalten sein sollen. |

### Beispiele

Zeigt, wie der Feldcode eines Felds abgerufen wird.

```csharp
// Öffne ein Dokument, das ein MERGEFIELD in einem IF-Feld enthält.
Document doc = new Document(MyDir + "Nested fields.docx");
FieldIf fieldIf = (FieldIf)doc.Range.Fields[0];

// Es gibt zwei Möglichkeiten, den Feldcode eines Felds zu erhalten:
// 1 - Lassen Sie die inneren Felder weg:
Assert.AreEqual(" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf.GetFieldCode(false));

// 2 - Fügen Sie die inneren Felder hinzu:
Assert.AreEqual($" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" ",
    fieldIf.GetFieldCode(true));

// Standardmäßig zeigt die GetFieldCode-Methode innere Felder an.
Assert.AreEqual(fieldIf.GetFieldCode(), fieldIf.GetFieldCode(true));
```

### Siehe auch

* class [Field](../)
* namensraum [Aspose.Words.Fields](../../field/)
* Montage [Aspose.Words](../../../)


