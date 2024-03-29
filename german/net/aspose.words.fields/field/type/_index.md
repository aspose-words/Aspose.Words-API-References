---
title: Field.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words für .NET
description: Field Type eigendom. Ruft den Microsoft WordFeldtyp ab in C#.
type: docs
weight: 100
url: /de/net/aspose.words.fields/field/type/
---
## Field.Type property

Ruft den Microsoft Word-Feldtyp ab.

```csharp
public virtual FieldType Type { get; }
```

## Beispiele

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

* enum [FieldType](../../fieldtype/)
* class [Field](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
