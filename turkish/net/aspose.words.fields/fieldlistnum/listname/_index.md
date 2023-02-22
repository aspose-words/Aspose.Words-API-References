---
title: FieldListNum.ListName
second_title: Aspose.Words for .NET API Referansı
description: FieldListNum mülk. Numaralandırma için kullanılan soyut numaralandırma tanımının adını alır veya ayarlar.
type: docs
weight: 40
url: /tr/net/aspose.words.fields/fieldlistnum/listname/
---
## FieldListNum.ListName property

Numaralandırma için kullanılan soyut numaralandırma tanımının adını alır veya ayarlar.

```csharp
public string ListName { get; set; }
```

### Örnekler

LISTNUM alanlarıyla paragrafların nasıl numaralandırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// LISTNUM alanları, her LISTNUM alanında artan bir sayı görüntüler.
// Bu alanlar ayrıca, onları numaralı listeleri taklit etmek için kullanmamıza izin veren çeşitli seçeneklere sahiptir.
FieldListNum field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);

// Listeler varsayılan olarak 1'den saymaya başlar, ancak bu sayıyı 0 gibi farklı bir değere ayarlayabiliriz.
// Bu alan "0)" gösterecektir.
field.StartingNumber = "0";
builder.Writeln("Paragraph 1");

Assert.AreEqual(" LISTNUM  \\s 0", field.GetFieldCode());

 // LISTNUM alanları, her liste düzeyi için ayrı sayıları korur.
// LISTNUM alanını başka bir LISTNUM alanıyla aynı paragrafa ekleme
// sayı yerine liste düzeyini artırır.
// Bir sonraki alan yukarıda başlattığımız sayıma devam edecek ve liste düzeyinde 1 değerini gösterecek.
builder.InsertField(FieldType.FieldListNum, true);

// Bu alan liste düzeyinde bir sayıma başlar. "1" değerini görüntüler.
builder.InsertField(FieldType.FieldListNum, true);

// Bu alan liste düzeyinde bir sayıma başlar. "1" değerini görüntüler.
// Farklı liste düzeylerinin farklı biçimlendirmeleri vardır,
// böylece bu alanlar birleştirilmiş "1)a)i)" değerini gösterecek.
builder.InsertField(FieldType.FieldListNum, true);
builder.Writeln("Paragraph 2");

// Ekleyeceğimiz sonraki LISTNUM alanı, saymaya liste düzeyinde devam edecek
// önceki LISTNUM alanının açık olduğunu.
// Farklı bir liste düzeyine atlamak için "ListLevel" özelliğini kullanabiliriz.
// Bu LISTNUM alanı 3. liste seviyesinde kalsaydı, "ii)" gösterirdi,
// ancak 2. listeye taşıdığımız için saymaya o seviyede devam ediyor ve "b)" gösteriyor.
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListLevel = "2";
builder.Writeln("Paragraph 3");

Assert.AreEqual(" LISTNUM  \\l 2", field.GetFieldCode());

// Alanın farklı bir AUTONUM alan türüne öykünmesini sağlamak için ListName özelliğini ayarlayabiliriz.
// "NumberDefault", AUTONUM'a öykünür, "OutlineDefault", AUTONUMOUT'a öykünür,
// ve "LegalDefault", AUTONUMLGL alanlarını öykünür.
// Başlangıç numarası 1 olan "OutlineDefault" liste adı, "I" öğesinin görüntülenmesine neden olur.
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.StartingNumber = "1";
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 4");

Assert.IsTrue(field.HasListName);
Assert.AreEqual(" LISTNUM  OutlineDefault \\s 1", field.GetFieldCode());

// ListName önceki alandan taşınmaz, bu yüzden her yeni alan için onu ayarlamamız gerekecek.
// Bu alan saymaya farklı liste adı ile devam eder ve "II." gösterir.
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


