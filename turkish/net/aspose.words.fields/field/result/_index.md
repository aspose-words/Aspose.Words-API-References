---
title: Field.Result
linktitle: Result
articleTitle: Result
second_title: .NET için Aspose.Words
description: Alan Sonuç özelliklerini zahmetsizce yönetin. Kolaylaştırılmış veri işleme ve gelişmiş verimlilik için alan ayırıcıları arasındaki metne erişin veya metni değiştirin.
type: docs
weight: 70
url: /tr/net/aspose.words.fields/field/result/
---
## Field.Result property

Alan ayırıcısı ile alan sonu arasındaki metni alır veya ayarlar.

```csharp
public string Result { get; set; }
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

* class [Field](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
