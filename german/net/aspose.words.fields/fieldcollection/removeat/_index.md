---
title: FieldCollection.RemoveAt
second_title: Aspose.Words für .NET-API-Referenz
description: FieldCollection methode. Entfernt ein Feld am angegebenen Index aus dieser Sammlung und aus dem Dokument.
type: docs
weight: 60
url: /de/net/aspose.words.fields/fieldcollection/removeat/
---
## FieldCollection.RemoveAt method

Entfernt ein Feld am angegebenen Index aus dieser Sammlung und aus dem Dokument.

```csharp
public void RemoveAt(int index)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| index | Int32 | Ein Index in die Sammlung. |

### Beispiele

Zeigt, wie Felder aus einer Feldsammlung entfernt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
builder.InsertField(" TIME ");
builder.InsertField(" REVNUM ");
builder.InsertField(" AUTHOR  \"John Doe\" ");
builder.InsertField(" SUBJECT \"My Subject\" ");
builder.InsertField(" QUOTE \"Hello world!\" ");
doc.UpdateFields();

FieldCollection fields = doc.Range.Fields;

Assert.AreEqual(6, fields.Count);

// Im Folgenden finden Sie vier Möglichkeiten zum Entfernen von Feldern aus einer Feldsammlung.
// 1 - Holen Sie sich ein Feld, um sich selbst zu entfernen:
fields[0].Remove();
Assert.AreEqual(5, fields.Count);

// 2 - Holen Sie sich die Sammlung, um ein Feld zu entfernen, das wir an seine Entfernungsmethode übergeben:
Field lastField = fields[3];
fields.Remove(lastField);
Assert.AreEqual(4, fields.Count);

// 3 - Entfernen Sie ein Feld aus einer Sammlung an einem Index:
fields.RemoveAt(2);
Assert.AreEqual(3, fields.Count);

// 4 - Alle Felder auf einmal aus der Sammlung entfernen:
fields.Clear();
Assert.AreEqual(0, fields.Count);
```

### Siehe auch

* class [FieldCollection](../)
* namensraum [Aspose.Words.Fields](../../fieldcollection/)
* Montage [Aspose.Words](../../../)


