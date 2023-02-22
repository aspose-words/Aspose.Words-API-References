---
title: FieldToc.SequenceSeparator
second_title: Aspose.Words for .NET API Referansı
description: FieldToc mülk. Sıra numaralarını ve sayfa numaralarını ayırmak için kullanılan karakter sırasını alır veya ayarlar.
type: docs
weight: 150
url: /tr/net/aspose.words.fields/fieldtoc/sequenceseparator/
---
## FieldToc.SequenceSeparator property

Sıra numaralarını ve sayfa numaralarını ayırmak için kullanılan karakter sırasını alır veya ayarlar.

```csharp
public string SequenceSeparator { get; set; }
```

### Örnekler

Bir TOC alanının SEQ alanlarını kullanarak girişlerle nasıl doldurulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir TOC alanı, belgede bulunan her SEQ alanı için içindekiler tablosunda bir giriş oluşturabilir.
// Her giriş, SEQ alanını içeren paragrafı ve alanın göründüğü sayfanın numarasını içerir.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// SEQ alanları, her SEQ alanında artan bir sayı görüntüler.
// Bu alanlar ayrıca her benzersiz adlandırılmış dizi için ayrı sayılar tutar
// SEQ alanının "SequenceIdentifier" özelliği ile tanımlanır.
// İçindekiler için bir ana diziyi adlandırmak için "TableOf FiguresLabel" özelliğini kullanın.
// Şimdi, bu TOC, yalnızca "SequenceIdentifier", "MySequence" olarak ayarlanmış SEQ alanlarından girişler oluşturacaktır.
fieldToc.TableOfFiguresLabel = "MySequence";

// "PrefixedSequenceIdentifier" özelliğinde başka bir SEQ alan dizisine isim verebiliriz.
 // Bu önek dizisindeki SEQ alanları, TOC girişleri oluşturmayacaktır.
// Bir ana dizi SEQ alanından oluşturulan her TOC girişi şimdi aynı zamanda
// ön ek dizisi şu anda girişi yapan birincil dizi SEQ alanında açık.
fieldToc.PrefixedSequenceIdentifier = "PrefixSequence";

// Her TOC girişi, hemen solda önek dizisi sayısını görüntüler
// ana sıra SEQ alanının göründüğü sayfa numarasının.
// Bu iki sayı arasında görünecek özel bir ayırıcı belirtebiliriz.
fieldToc.SequenceSeparator = ">";

Assert.AreEqual(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);

// Bu TOC'yi doldurmak için SEQ alanlarını kullanmanın iki yolu vardır.
// 1 - İçindekiler'in önek dizisine ait bir SEQ alanı ekleme:
// Bu alan, "PrefixSequence" için SEQ dizi sayısını 1 artıracaktır.
// Bu alan tanımlanan ana diziye ait olmadığı için
// TOC'nin "TableOf FiguresLabel" özelliği ile girdi olarak görünmeyecektir.
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();

Assert.AreEqual(" SEQ  PrefixSequence", fieldSeq.GetFieldCode());

// 2 - İçindekiler'in ana dizisine ait bir SEQ alanı ekleme:
// Bu SEQ alanı, TOC'de bir giriş yaratacaktır.
// TOC girişi, SEQ alanının bulunduğu paragrafı ve göründüğü sayfanın numarasını içerecektir.
// Bu giriş aynı zamanda önek dizisinin şu anda bulunduğu sayıyı da gösterecektir,
// İçindekiler'in SeqenceSeparator özelliğindeki değerle sayfa numarasından ayrılır.
// "PrefixSequence" sayısı 1'dir, bu ana dizi SEQ alanı 2. sayfadadır,
// ve ayırıcı ">", yani giriş "1>2" görüntüleyecektir.
builder.Write("First TOC entry, MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", fieldSeq.GetFieldCode());

// Bir sayfa ekleyin, önek dizisini 2 ile ilerletin ve ardından bir TOC girişi oluşturmak için bir SEQ alanı ekleyin.
// Ön ek dizisi şimdi 2'de ve ana dizi SEQ alanı 3. sayfada,
// böylece TOC girişi sayfa sayısında "2>3" görüntüleyecektir.
builder.InsertBreak(BreakType.PageBreak);
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
builder.Write("Second TOC entry, MySequence #");
fieldSeq.SequenceIdentifier = "MySequence";

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.TOC.SEQ.docx");
```

### Ayrıca bakınız

* class [FieldToc](../)
* ad alanı [Aspose.Words.Fields](../../fieldtoc/)
* toplantı [Aspose.Words](../../../)


