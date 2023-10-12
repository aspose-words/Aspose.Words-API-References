---
title: Field.Result
second_title: Aspose.Words für .NET-API-Referenz
description: Field eigendom. Ruft Text ab der zwischen dem Feldtrennzeichen und dem Feldende liegt oder legt diesen fest.
type: docs
weight: 70
url: /de/net/aspose.words.fields/field/result/
---
## Field.Result property

Ruft Text ab, der zwischen dem Feldtrennzeichen und dem Feldende liegt, oder legt diesen fest.

```csharp
public string Result { get; set; }
```

### Beispiele

Zeigt, wie man mithilfe eines Feldcodes ein Feld in ein Dokument einfügt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Diese Überladung der InsertField-Methode aktualisiert automatisch eingefügte Felder.
Assert.That(DateTime.Parse(field.Result), Is.EqualTo(DateTime.Today).Within(1).Days);
```

### Siehe auch

* class [Field](../)
* namensraum [Aspose.Words.Fields](../../field/)
* Montage [Aspose.Words](../../../)


