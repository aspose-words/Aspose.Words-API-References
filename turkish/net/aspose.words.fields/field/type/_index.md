---
title: Field.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words for .NET
description: Field Type mülk. Microsoft Word alan türünü alır C#'da.
type: docs
weight: 100
url: /tr/net/aspose.words.fields/field/type/
---
## Field.Type property

Microsoft Word alan türünü alır.

```csharp
public virtual FieldType Type { get; }
```

## Örnekler

Alan kodu kullanarak belgeye nasıl alan ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// InsertField yönteminin bu aşırı yüklemesi, eklenen alanları otomatik olarak günceller.
Assert.That(DateTime.Parse(field.Result), Is.EqualTo(DateTime.Today).Within(1).Days);
```

### Ayrıca bakınız

* enum [FieldType](../../fieldtype/)
* class [Field](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
