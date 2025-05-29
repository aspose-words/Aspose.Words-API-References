---
title: Document.NormalizeFieldTypes
linktitle: NormalizeFieldTypes
articleTitle: NormalizeFieldTypes
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihr Dokument mit der Methode „NormalizeFieldTypes“ und stellen Sie sicher, dass alle Feldtypwerte mit den Feldcodes übereinstimmen, um die Konsistenz und Genauigkeit zu verbessern.
type: docs
weight: 670
url: /de/net/aspose.words/document/normalizefieldtypes/
---
## Document.NormalizeFieldTypes method

Ändert Feldtypwerte[`FieldType`](../../../aspose.words.fields/fieldchar/fieldtype/) von[`FieldStart`](../../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../../aspose.words.fields/fieldend/) im gesamten Dokument, sodass sie den in den Feldfunktionen enthaltenen Feldtypen entsprechen.

```csharp
public void NormalizeFieldTypes()
```

## Bemerkungen

Verwenden Sie diese Methode nach Dokumentänderungen, die Feldtypen betreffen.

Um Feldtypwerte in einem bestimmten Teil des Dokuments zu ändern, verwenden Sie[`NormalizeFieldTypes`](../../range/normalizefieldtypes/).

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

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
