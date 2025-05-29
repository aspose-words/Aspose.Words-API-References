---
title: Field.GetFieldCode
linktitle: GetFieldCode
articleTitle: GetFieldCode
second_title: Aspose.Words für .NET
description: Entdecken Sie die GetFieldCode-Methode, mit der Sie mühelos Text zwischen Feldanfang und Trennzeichen abrufen können, einschließlich der Codes der untergeordneten Felder und der Ergebnisse. Steigern Sie Ihre Codiereffizienz!
type: docs
weight: 110
url: /de/net/aspose.words.fields/field/getfieldcode/
---
## GetFieldCode() {#getfieldcode}

Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldergebnis von untergeordneten Feldern werden einbezogen.

```csharp
public string GetFieldCode()
```

## Beispiele

Zeigt, wie Sie mithilfe eines Feldcodes ein Feld in ein Dokument einfügen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Diese Überladung der InsertField-Methode aktualisiert eingefügte Felder automatisch.
Assert.True((DateTime.Today - DateTime.Parse(field.Result)).Days <= 1);
```

Zeigt, wie man den Feldcode eines Felds erhält.

```csharp
// Öffnen Sie ein Dokument, das ein MERGEFIELD innerhalb eines IF-Feldes enthält.
Document doc = new Document(MyDir + "Nested fields.docx");
FieldIf fieldIf = (FieldIf)doc.Range.Fields[0];

// Es gibt zwei Möglichkeiten, den Feldcode eines Feldes zu erhalten:
// 1 – Lassen Sie die inneren Felder weg:
Assert.AreEqual(" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf.GetFieldCode(false));

// 2 - Schließen Sie die inneren Felder ein:
Assert.AreEqual($" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" ",
    fieldIf.GetFieldCode(true));

// Standardmäßig zeigt die Methode GetFieldCode innere Felder an.
Assert.AreEqual(fieldIf.GetFieldCode(), fieldIf.GetFieldCode(true));
```

### Siehe auch

* class [Field](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)

---

## GetFieldCode(*bool*) {#getfieldcode_1}

Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist).

```csharp
public string GetFieldCode(bool includeChildFieldCodes)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| includeChildFieldCodes | Boolean | `WAHR` ob untergeordnete Feldcodes einbezogen werden sollen. |

## Beispiele

Zeigt, wie man den Feldcode eines Felds erhält.

```csharp
// Öffnen Sie ein Dokument, das ein MERGEFIELD innerhalb eines IF-Feldes enthält.
Document doc = new Document(MyDir + "Nested fields.docx");
FieldIf fieldIf = (FieldIf)doc.Range.Fields[0];

// Es gibt zwei Möglichkeiten, den Feldcode eines Feldes zu erhalten:
// 1 – Lassen Sie die inneren Felder weg:
Assert.AreEqual(" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf.GetFieldCode(false));

// 2 - Schließen Sie die inneren Felder ein:
Assert.AreEqual($" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" ",
    fieldIf.GetFieldCode(true));

// Standardmäßig zeigt die Methode GetFieldCode innere Felder an.
Assert.AreEqual(fieldIf.GetFieldCode(), fieldIf.GetFieldCode(true));
```

### Siehe auch

* class [Field](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
