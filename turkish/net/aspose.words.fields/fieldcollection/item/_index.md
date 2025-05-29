---
title: FieldCollection.Item
linktitle: Item
articleTitle: Item
second_title: .NET için Aspose.Words
description: FieldCollection Item özelliğini keşfedin, alanlara indekse göre zahmetsizce erişin ve veri yönetiminizi kolay ve hassas bir şekilde geliştirin.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldcollection/item/
---
## FieldCollection indexer

Belirtilen dizinde bir alan döndürür.

```csharp
public Field this[int index] { get; }
```

| Parametre | Tanım |
| --- | --- |
| index | Koleksiyonun indeksi. |

## Notlar

Endeks sıfır bazlıdır.

Negatif indekslere izin verilir ve koleksiyonun sonundan erişimi belirtir. Örneğin -1 son öğeyi, -2 sondan bir önceki öğeyi vb. ifade eder.

Eğer indeks listedeki öğe sayısından büyük veya eşitse, bu boş bir referans döndürür.

Eğer indeks negatifse ve mutlak değeri listedeki öğe sayısından büyükse, bu durum boş bir referans döndürür.

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
