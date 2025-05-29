---
title: FieldCollection.Remove
linktitle: Remove
articleTitle: Remove
second_title: .NET için Aspose.Words
description: FieldCollection Remove yöntemi ile belirli alanları belgenizden zahmetsizce kaldırarak veri yönetimi sürecinizi hızlandırın.
type: docs
weight: 50
url: /tr/net/aspose.words.fields/fieldcollection/remove/
---
## FieldCollection.Remove method

Belirtilen alanı bu koleksiyondan ve belgeden kaldırır.

```csharp
public void Remove(Field field)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| field | Field | Kaldırılacak bir alan. |

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

* class [Field](../../field/)
* class [FieldCollection](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
