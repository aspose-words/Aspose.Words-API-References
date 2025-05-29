---
title: Field.Type
linktitle: Type
articleTitle: Type
second_title: .NET için Aspose.Words
description: Alan Türü özelliğimizle Microsoft Word alan türünü keşfedin. Belgelerinizi hassas biçimlendirme ve dinamik içerik yetenekleriyle geliştirin.
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

Alan kodu kullanılarak bir belgeye alanın nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// InsertField yönteminin bu aşırı yüklemesi eklenen alanları otomatik olarak günceller.
Assert.True((DateTime.Today - DateTime.Parse(field.Result)).Days <= 1);
```

### Ayrıca bakınız

* enum [FieldType](../../fieldtype/)
* class [Field](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
