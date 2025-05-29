---
title: Field.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words für .NET
description: Entdecken Sie den Microsoft Word-Feldtyp mit unserer Feldtyp-Eigenschaft. Optimieren Sie Ihre Dokumente mit präziser Formatierung und dynamischen Inhaltsfunktionen.
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

* enum [FieldType](../../fieldtype/)
* class [Field](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
