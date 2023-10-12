---
title: FieldListNum.StartingNumber
second_title: Aspose.Words for .NET API Referansı
description: FieldListNum mülk. Bu alanın başlangıç değerini alır veya ayarlar.
type: docs
weight: 50
url: /tr/net/aspose.words.fields/fieldlistnum/startingnumber/
---
## FieldListNum.StartingNumber property

Bu alanın başlangıç değerini alır veya ayarlar.

```csharp
public string StartingNumber { get; set; }
```

### Örnekler

LISTNUM alanlarıyla paragrafların nasıl numaralandırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// LISTNUM alanları, her LISTNUM alanında artan bir sayı görüntüler.
// Bu alanlar aynı zamanda onları numaralandırılmış listeleri taklit etmek için kullanmamıza izin veren çeşitli seçeneklere de sahiptir.
FieldListNum field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);

// Listeler varsayılan olarak 1'den saymaya başlar ancak bu sayıyı 0 gibi farklı bir değere de ayarlayabiliriz.
// Bu alanda "0)" görüntülenecektir.
field.StartingNumber = "0";
builder.Writeln("Paragraph 1");

Assert.AreEqual(" LISTNUM  \\s 0", field.GetFieldCode());

 // LISTNUM alanları her liste düzeyi için ayrı sayıları korur.
// LISTNUM alanını başka bir LISTNUM alanıyla aynı paragrafa ekleme
// sayı yerine liste düzeyini artırır.
// Bir sonraki alan yukarıda başlattığımız sayıma devam edecek ve liste düzeyi 1'de "1" değerini görüntüleyecektir.
builder.InsertField(FieldType.FieldListNum, true);

// Bu alan liste düzeyinde 2'den bir sayım başlatacaktır. "1" değerini görüntüleyecektir.
builder.InsertField(FieldType.FieldListNum, true);

// Bu alan liste düzeyinde 3'ten bir sayım başlatacaktır. "1" değerini görüntüleyecektir.
// Farklı liste seviyelerinin farklı formatları vardır,
// böylece bu alanlar bir araya getirildiğinde "1)a)i)" değeri görüntülenecektir.
builder.InsertField(FieldType.FieldListNum, true);
builder.Writeln("Paragraph 2");

// Ekleyeceğimiz bir sonraki LISTNUM alanı liste düzeyinde sayıma devam edecek
// önceki LISTNUM alanının açık olduğu.
// Farklı bir liste düzeyine atlamak için "ListLevel" özelliğini kullanabiliriz.
// Bu LISTNUM alanı liste düzeyi 3'te kalırsa "ii)" görüntülenir,
// ama liste düzeyi 2'ye taşıdığımız için o düzeyde saymaya devam ediyor ve "b)" gösteriyor.
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListLevel = "2";
builder.Writeln("Paragraph 3");

Assert.AreEqual(" LISTNUM  \\l 2", field.GetFieldCode());

// Alanın farklı bir AUTONUM alan tipini taklit etmesini sağlamak için ListName özelliğini ayarlayabiliriz.
// "NumberDefault" AUTONUM'u taklit eder, "OutlineDefault" AUTONUMOUT'u taklit eder,
// ve "LegalDefault", AUTONUMLGL alanlarını taklit eder.
// Başlangıç numarası 1 olan "OutlineDefault" liste adı, "I." görüntülenmesiyle sonuçlanacaktır.
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.StartingNumber = "1";
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 4");

Assert.IsTrue(field.HasListName);
Assert.AreEqual(" LISTNUM  OutlineDefault \\s 1", field.GetFieldCode());

// ListName önceki alandan taşınmaz, dolayısıyla onu her yeni alan için ayarlamamız gerekecek.
// Bu alan farklı liste adı ile sayıma devam eder ve "II." değerini görüntüler.
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 5");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.LISTNUM.docx");
```

### Ayrıca bakınız

* class [FieldListNum](../)
* ad alanı [Aspose.Words.Fields](../../fieldlistnum/)
* toplantı [Aspose.Words](../../../)


