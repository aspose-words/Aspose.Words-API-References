---
title: Range.NormalizeFieldTypes
linktitle: NormalizeFieldTypes
articleTitle: NormalizeFieldTypes
second_title: Aspose.Words für .NET
description: Transformieren Sie Feldtypen mit der Methode „NormalizeFieldTypes“. Stellen Sie sicher, dass FieldStart, FieldSeparator und FieldEnd mit den angegebenen Feldcodes übereinstimmen, um eine reibungslose Datenverarbeitung zu gewährleisten.
type: docs
weight: 90
url: /de/net/aspose.words/range/normalizefieldtypes/
---
## Range.NormalizeFieldTypes method

Ändert Feldtypwerte[`FieldType`](../../../aspose.words.fields/fieldchar/fieldtype/) von[`FieldStart`](../../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../../aspose.words.fields/fieldend/) in diesem Bereich, sodass sie den in den Feldcodes enthaltenen Feldtypen entsprechen.

```csharp
public void NormalizeFieldTypes()
```

## Bemerkungen

Verwenden Sie diese Methode nach Dokumentänderungen, die Feldtypen betreffen.

Um Feldtypwerte im gesamten Dokument zu ändern, verwenden Sie[`NormalizeFieldTypes`](../../document/normalizefieldtypes/).

## Beispiele

Zeigt, wie der Typ eines Felds mit seinem Feldcode auf dem neuesten Stand gehalten wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE", null);

// Aspose.Words erkennt Feldtypen automatisch anhand von Feldcodes.
Assert.AreEqual(FieldType.FieldDate, field.Type);

// Ändern Sie manuell den Rohtext des Feldes, der den Feldcode bestimmt.
Run fieldText = (Run)doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Run, true)[0];
fieldText.Text = "PAGE";

// Durch die Änderung des Feldcodes wurde dieses Feld in ein Feld eines anderen Typs geändert.
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

* class [Range](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
