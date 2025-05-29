---
title: FieldCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: .NET için Aspose.Words
description: FieldCollection RemoveAt yöntemiyle belgenizden alanları zahmetsizce kaldırın. Veri yönetiminizi bugün kolaylaştırın!
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
| index | Int32 | Koleksiyonun indeksi. |

## Örnekler

Bir alan koleksiyonundan alanların nasıl kaldırılacağını gösterir.

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

// Aşağıda bir alan koleksiyonundan alanları kaldırmanın dört yolu bulunmaktadır.
// 1 - Bir alanın kendisini kaldırmasını sağla:
fields[0].Remove();
Assert.AreEqual(5, fields.Count);

// 2 - Kaldırma yöntemine geçirdiğimiz bir alanı kaldırmak için koleksiyonu edinin:
Field lastField = fields[3];
fields.Remove(lastField);
Assert.AreEqual(4, fields.Count);

// 3 - Bir dizindeki bir koleksiyondan bir alanı kaldır:
fields.RemoveAt(2);
Assert.AreEqual(3, fields.Count);

// 4 - Koleksiyondaki tüm alanları aynı anda kaldır:
fields.Clear();
Assert.AreEqual(0, fields.Count);
```

### Ayrıca bakınız

* class [FieldCollection](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
