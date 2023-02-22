---
title: FieldCollection.RemoveAt
second_title: Aspose.Words for .NET API Referansı
description: FieldCollection yöntem. Belirtilen dizindeki bir alanı bu koleksiyondan ve belgeden kaldırır.
type: docs
weight: 60
url: /tr/net/aspose.words.fields/fieldcollection/removeat/
---
## FieldCollection.RemoveAt method

Belirtilen dizindeki bir alanı bu koleksiyondan ve belgeden kaldırır.

```csharp
public void RemoveAt(int index)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| index | Int32 | Koleksiyona bir dizin. |

### Örnekler

Alan koleksiyonundan alanların nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
builder.InsertField(" TIME ");
builder.InsertField(" REVNUM ");
builder.InsertField(" AUTHOR  \"John Doe\" ");
builder.InsertField(" SUBJECT \"My Subject\" ");
builder.InsertField(" QUOTE \"Hello world!\" ");
doc.UpdateFields();

FieldCollection fields = doc.Range.Fields;

Assert.AreEqual(6, fields.Count);

// Bir alan koleksiyonundan alanları kaldırmanın dört yolu aşağıdadır.
// 1 - Kendisini kaldırmak için bir alan alın:
fields[0].Remove();
Assert.AreEqual(5, fields.Count);

// 2 - Kaldırma yöntemine ilettiğimiz bir alanı kaldırmak için koleksiyonu alın:
Field lastField = fields[3];
fields.Remove(lastField);
Assert.AreEqual(4, fields.Count);

// 3 - Bir dizindeki koleksiyondan bir alanı kaldırın:
fields.RemoveAt(2);
Assert.AreEqual(3, fields.Count);

// 4 - Koleksiyondaki tüm alanları bir kerede kaldırın:
fields.Clear();
Assert.AreEqual(0, fields.Count);
```

### Ayrıca bakınız

* class [FieldCollection](../)
* ad alanı [Aspose.Words.Fields](../../fieldcollection/)
* toplantı [Aspose.Words](../../../)


