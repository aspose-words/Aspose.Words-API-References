---
title: Field.IsLocked
linktitle: IsLocked
articleTitle: IsLocked
second_title: Aspose.Words für .NET
description: Entdecken Sie die IsLocked-Eigenschaft für Felder – steuern Sie Neuberechnungen und verbessern Sie die Datenintegrität. Profitieren Sie noch heute von einer effizienten Verwaltung Ihrer Datenergebnisse!
type: docs
weight: 50
url: /de/net/aspose.words.fields/field/islocked/
---
## Field.IsLocked property

Ruft ab oder legt fest, ob das Feld gesperrt ist (das Ergebnis sollte nicht neu berechnet werden).

```csharp
public bool IsLocked { get; set; }
```

## Beispiele

Zeigt, wie mit einem FieldStart-Knoten gearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldDate field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.Format.DateTimeFormat = "dddd, MMMM dd, yyyy";
field.Update();

FieldChar fieldStart = field.Start;

Assert.AreEqual(FieldType.FieldDate, fieldStart.FieldType);
Assert.AreEqual(false, fieldStart.IsDirty);
Assert.AreEqual(false, fieldStart.IsLocked);

// Ruft das Fassadenobjekt ab, das das Feld im Dokument darstellt.
field = (FieldDate)fieldStart.GetField();

Assert.AreEqual(false, field.IsLocked);
Assert.AreEqual(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Aktualisieren Sie das Feld, um das aktuelle Datum anzuzeigen.
field.Update();
```

### Siehe auch

* class [Field](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
