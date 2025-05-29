---
title: FieldCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: Aspose.Words für .NET
description: Entfernen Sie mühelos Felder aus Ihrem Dokument mit der Methode „FieldCollection RemoveAt“. Optimieren Sie noch heute Ihr Datenmanagement!
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
| index | Int32 | Ein Index zur Sammlung. |

## Beispiele

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

// Unten sind vier Möglichkeiten zum Entfernen von Feldern aus einer Feldsammlung aufgeführt.
// 1 - Ein Feld dazu bringen, sich selbst zu entfernen:
fields[0].Remove();
Assert.AreEqual(5, fields.Count);

// 2 – Lassen Sie die Sammlung ein Feld entfernen, das wir an ihre Entfernungsmethode übergeben:
Field lastField = fields[3];
fields.Remove(lastField);
Assert.AreEqual(4, fields.Count);

// 3 – Entfernen Sie ein Feld aus einer Sammlung an einem Index:
fields.RemoveAt(2);
Assert.AreEqual(3, fields.Count);

// 4 – Entfernen Sie alle Felder auf einmal aus der Sammlung:
fields.Clear();
Assert.AreEqual(0, fields.Count);
```

### Siehe auch

* class [FieldCollection](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
