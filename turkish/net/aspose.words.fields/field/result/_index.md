---
title: Field.Result
linktitle: Result
articleTitle: Result
second_title: Aspose.Words for .NET
description: Field Result mülk. Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar C#'da.
type: docs
weight: 70
url: /tr/net/aspose.words.fields/field/result/
---
## Field.Result property

Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar.

```csharp
public string Result { get; set; }
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

* class [Field](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
