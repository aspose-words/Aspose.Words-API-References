---
title: Document.NormalizeFieldTypes
second_title: Aspose.Words für .NET-API-Referenz
description: Document methode. Ändert FeldtypwerteFieldType vonFieldStart FieldSeparator FieldEnd im gesamten Dokument damit sie den in den Feldcodes enthaltenen Feldtypen entsprechen.
type: docs
weight: 610
url: /de/net/aspose.words/document/normalizefieldtypes/
---
## Document.NormalizeFieldTypes method

Ändert Feldtypwerte[`FieldType`](../../../aspose.words.fields/fieldchar/fieldtype/) von[`FieldStart`](../../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../../aspose.words.fields/fieldend/) im gesamten Dokument, damit sie den in den Feldcodes enthaltenen Feldtypen entsprechen.

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

// Aspose.Words erkennt automatisch Feldtypen basierend auf Feldcodes.
Assert.AreEqual(FieldType.FieldDate, field.Type);

// Ändern Sie manuell den Rohtext des Felds, der den Feldcode bestimmt.
Run fieldText = (Run)doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Run, true)[0];

// Das Ändern des Feldcodes hat dieses Feld in einen anderen Typ geändert,
// aber die Typeigenschaften des Felds zeigen immer noch den alten Typ an.
Assert.AreEqual("PAGE", field.GetFieldCode());
Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual(FieldType.FieldDate, field.Start.FieldType);
Assert.AreEqual(FieldType.FieldDate, field.Separator.FieldType);
Assert.AreEqual(FieldType.FieldDate, field.End.FieldType);

// Aktualisieren Sie diese Eigenschaften mit dieser Methode, um den aktuellen Wert anzuzeigen.
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


