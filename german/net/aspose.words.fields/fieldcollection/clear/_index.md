---
title: FieldCollection.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words für .NET
description: Löschen Sie mühelos alle Felder aus Ihrer FieldCollection mit unserer Clear-Methode. Optimieren Sie Ihr Dokumentenmanagement und steigern Sie noch heute die Effizienz!
type: docs
weight: 30
url: /de/net/aspose.words.fields/fieldcollection/clear/
---
## FieldCollection.Clear method

Entfernt alle Felder dieser Sammlung aus dem Dokument und aus dieser Sammlung selbst.

```csharp
public void Clear()
```

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
