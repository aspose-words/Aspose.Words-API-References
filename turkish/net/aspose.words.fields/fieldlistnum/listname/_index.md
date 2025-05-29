---
title: FieldListNum.ListName
linktitle: ListName
articleTitle: ListName
second_title: .NET için Aspose.Words
description: Gelişmiş belge organizasyonu ve netliği için soyut numaralandırma tanımlarını kolayca yönetmek üzere FieldListNum ListName özelliğini keşfedin.
type: docs
weight: 40
url: /tr/net/aspose.words.fields/fieldlistnum/listname/
---
## FieldListNum.ListName property

Numaralandırma için kullanılan soyut numaralandırma tanımının adını alır veya ayarlar.

```csharp
public string ListName { get; set; }
```

## Örnekler

LISTNUM alanlarıyla paragrafların nasıl numaralandırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// LISTNUM alanları, her LISTNUM alanında artan bir sayı görüntüler.
// Bu alanlar ayrıca numaralandırılmış listeleri taklit etmemize olanak tanıyan çeşitli seçeneklere sahiptir.
FieldListNum field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);

// Listeler varsayılan olarak 1'den saymaya başlar, ancak bu sayıyı 0 gibi farklı bir değere ayarlayabiliriz.
// Bu alanda "0)" gösterilecektir.
field.StartingNumber = "0";
builder.Writeln("Paragraph 1");

Assert.AreEqual(" LISTNUM  \\s 0", field.GetFieldCode());

// LISTNUM alanları her liste düzeyi için ayrı sayımları korur.
// Aynı paragrafa başka bir LISTNUM alanıyla birlikte bir LISTNUM alanı ekleme
// sayım yerine liste düzeyini artırır.
// Bir sonraki alan yukarıda başlattığımız sayımı sürdürecek ve liste düzeyi 1'de "1" değerini gösterecektir.
builder.InsertField(FieldType.FieldListNum, true);

// Bu alan liste seviyesi 2'den itibaren sayımı başlatacaktır. "1" değerini gösterecektir.
builder.InsertField(FieldType.FieldListNum, true);

// Bu alan liste seviyesi 3'te bir sayım başlatacaktır. "1" değerini gösterecektir.
// Farklı liste seviyelerinin farklı biçimlendirmeleri vardır,
// bu alanların birleştirilmesiyle "1)a)i)" değeri görüntülenecektir.
builder.InsertField(FieldType.FieldListNum, true);
builder.Writeln("Paragraph 2");

// Eklediğimiz bir sonraki LISTNUM alanı sayımı liste düzeyinde sürdürecektir
// önceki LISTNUM alanının açık olduğu.
// Farklı bir liste düzeyine geçmek için "ListLevel" özelliğini kullanabiliriz.
// Bu LISTNUM alanı liste düzeyi 3'te kalsaydı, "ii)" görüntülenirdi,
// ancak, bunu liste düzeyi 2'ye taşıdığımız için, sayımı o düzeyde sürdürür ve "b)" görüntüler.
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListLevel = "2";
builder.Writeln("Paragraph 3");

Assert.AreEqual(" LISTNUM  \\l 2", field.GetFieldCode());

// Alanın farklı bir AUTONUM alan türünü taklit etmesini sağlamak için ListName özelliğini ayarlayabiliriz.
// "NumberDefault" AUTONUM'u taklit eder, "OutlineDefault" AUTONUMOUT'u taklit eder,
// ve "LegalDefault" AUTONUMLGL alanlarını taklit eder.
// Başlangıç numarası 1 olan "OutlineDefault" liste adı, "I." görüntülenmesiyle sonuçlanacaktır.
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.StartingNumber = "1";
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 4");

Assert.IsTrue(field.HasListName);
Assert.AreEqual(" LISTNUM  OutlineDefault \\s 1", field.GetFieldCode());

// ListName önceki alandan taşınmaz, bu yüzden her yeni alan için bunu ayarlamamız gerekecektir.
// Bu alan farklı liste adıyla sayımı sürdürür ve "II." görüntüler.
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 5");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.LISTNUM.docx");
```

### Ayrıca bakınız

* class [FieldListNum](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
