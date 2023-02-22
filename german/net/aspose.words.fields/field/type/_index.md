---
title: Field.Type
second_title: Aspose.Words für .NET-API-Referenz
description: Field eigendom. Ruft den Microsoft WordFeldtyp ab.
type: docs
weight: 100
url: /de/net/aspose.words.fields/field/type/
---
## Field.Type property

Ruft den Microsoft Word-Feldtyp ab.

```csharp
public virtual FieldType Type { get; }
```

### Beispiele

Zeigt, wie ein Feld mithilfe eines Feldcodes in ein Dokument eingefügt wird.

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

* enum [FieldType](../../fieldtype/)
* class [Field](../)
* namensraum [Aspose.Words.Fields](../../field/)
* Montage [Aspose.Words](../../../)


