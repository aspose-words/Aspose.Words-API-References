---
title: Field.Result
linktitle: Result
articleTitle: Result
second_title: Aspose.Words für .NET
description: Verwalten Sie Feldergebniseigenschaften mühelos. Greifen Sie auf Text zwischen Feldtrennzeichen zu oder ändern Sie ihn, um die Datenverarbeitung zu optimieren und die Effizienz zu steigern.
type: docs
weight: 70
url: /de/net/aspose.words.fields/field/result/
---
## Field.Result property

Ruft Text ab oder legt ihn fest, der zwischen Feldtrennzeichen und Feldende steht.

```csharp
public string Result { get; set; }
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

### Siehe auch

* class [Field](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
