---
title: Document.NormalizeFieldTypes
second_title: Aspose.Words für .NET-API-Referenz
description: Document methode. Ändert FeldtypwerteFieldType vonFieldStart FieldSeparator FieldEnd im gesamten Dokument sodass sie den in den Feldcodes enthaltenen Feldtypen entsprechen.
type: docs
weight: 650
url: /de/net/aspose.words/document/normalizefieldtypes/
---
## Document.NormalizeFieldTypes method

Ändert Feldtypwerte[`FieldType`](../../../aspose.words.fields/fieldchar/fieldtype/) von[`FieldStart`](../../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../../aspose.words.fields/fieldend/) im gesamten Dokument, sodass sie den in den Feldcodes enthaltenen Feldtypen entsprechen.

```csharp
public void NormalizeFieldTypes()
```

### Bemerkungen

Verwenden Sie diese Methode nach Dokumentänderungen, die sich auf Feldtypen auswirken.

Um Feldtypwerte in einem bestimmten Teil des Dokuments zu ändern, verwenden Sie[`NormalizeFieldTypes`](../../range/normalizefieldtypes/).

### Beispiele

Zeigt, wie Sie den Typ eines Felds mit seinem Feldcode auf dem neuesten Stand halten.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE", null);

// Aspose.Words erkennt Feldtypen automatisch anhand von Feldcodes.
Assert.AreEqual(FieldType.FieldDate, field.Type);

// Den Rohtext des Feldes manuell ändern, wodurch der Feldcode bestimmt wird.
Run fieldText = (Run)doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Run, true)[0];
fieldText.Text = "PAGE";

// Durch die Änderung des Feldcodes wurde dieses Feld in ein Feld mit einem anderen Typ geändert.
// aber die Typeigenschaften des Feldes zeigen immer noch den alten Typ an.
Assert.AreEqual("PAGE", field.GetFieldCode());
Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual(FieldType.FieldDate, field.Start.FieldType);
Assert.AreEqual(FieldType.FieldDate, field.Separator.FieldType);
Assert.AreEqual(FieldType.FieldDate, field.End.FieldType);

// Diese Eigenschaften mit dieser Methode aktualisieren, um den aktuellen Wert anzuzeigen.
doc.NormalizeFieldTypes();

Assert.AreEqual(FieldType.FieldPage, field.Type);
Assert.AreEqual(FieldType.FieldPage, field.Start.FieldType);
Assert.AreEqual(FieldType.FieldPage, field.Separator.FieldType); 
Assert.AreEqual(FieldType.FieldPage, field.End.FieldType);
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../document/)
* Montage [Aspose.Words](../../../)


