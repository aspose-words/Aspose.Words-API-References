---
title: FieldToc.PrefixedSequenceIdentifier
linktitle: PrefixedSequenceIdentifier
articleTitle: PrefixedSequenceIdentifier
second_title: .NET için Aspose.Words
description: FieldToc PrefixedSequenceIdentifier özelliğini keşfedin; sıra tanımlayıcılarını etkin bir şekilde yönetin ve girişinizin sayfa numarasını benzersiz öneklerle geliştirin.
type: docs
weight: 120
url: /tr/net/aspose.words.fields/fieldtoc/prefixedsequenceidentifier/
---
## FieldToc.PrefixedSequenceIdentifier property

Girişin sayfa numarasına bir önek eklenmesi gereken bir dizinin tanımlayıcısını alır veya ayarlar.

```csharp
public string PrefixedSequenceIdentifier { get; set; }
```

## Örnekler

İçindekiler alanının SEQ alanlarını kullanarak girdilerle nasıl doldurulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir TOC alanı, belgede bulunan her SEQ alanı için içerik tablosunda bir giriş oluşturabilir.
// Her girdi, SEQ alanını ve alanın göründüğü sayfa numarasını içeren paragrafı içerir.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// SEQ alanları her SEQ alanında artan bir sayım görüntüler.
// Bu alanlar ayrıca her benzersiz adlandırılmış dizi için ayrı sayımları korur
// SEQ alanının "SequenceIdentifier" özelliği ile tanımlanır.
// İçindekiler tablosunun ana dizisini adlandırmak için "TableOfFiguresLabel" özelliğini kullanın.
// Şimdi, bu İçindekiler tablosu yalnızca "SequenceIdentifier" değeri "MySequence" olarak ayarlanmış SEQ alanlarından girişler oluşturacaktır.
fieldToc.TableOfFiguresLabel = "MySequence";

// "PrefixedSequenceIdentifier" özelliğinde başka bir SEQ alan dizisi adlandırabiliriz.
 // Bu önek dizisinden gelen SEQ alanları TOC girişleri oluşturmaz.
// Ana dizi SEQ alanından oluşturulan her TOC girişi artık aynı zamanda sayıyı da görüntüleyecektir.
// ön ek dizisi şu anda girişi yapan birincil dizi SEQ alanında açık.
fieldToc.PrefixedSequenceIdentifier = "PrefixSequence";

// Her TOC girişi, hemen solunda önek dizisi sayısını görüntüler
// ana dizi SEQ alanının göründüğü sayfa numarasının.
// Bu iki sayının arasına gelecek özel bir ayraç belirleyebiliriz.
fieldToc.SequenceSeparator = ">";

Assert.AreEqual(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);

// Bu İçindekiler tablosunu doldurmak için SEQ alanlarını kullanmanın iki yolu vardır.
// 1 - TOC'nin önek dizisine ait bir SEQ alanı ekleniyor:
// Bu alan "PrefixSequence" için SEQ dizi sayısını 1 artıracaktır.
// Bu alan tanımlanan ana diziye ait olmadığından
// TOC'nin "TableOfFiguresLabel" özelliği sayesinde bir girdi olarak görünmeyecektir.
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();

Assert.AreEqual(" SEQ  PrefixSequence", fieldSeq.GetFieldCode());

// 2 - TOC'nin ana dizisine ait bir SEQ alanı ekleniyor:
// Bu SEQ alanı İçindekiler'de bir giriş oluşturacaktır.
// TOC girişi, SEQ alanının bulunduğu paragrafı ve göründüğü sayfanın numarasını içerecektir.
// Bu giriş ayrıca önek dizisinin şu anda bulunduğu sayıyı da görüntüler,
// sayfa numarasından TOC'nin SeqenceSeparator özelliğindeki değerle ayrılır.
// "PrefixSequence" sayısı 1'dir, bu ana dizi SEQ alanı 2. sayfadadır,
// ve ayraç ">" olduğundan, giriş "1>2" olarak görüntülenecektir.
builder.Write("First TOC entry, MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", fieldSeq.GetFieldCode());

// Bir sayfa ekle, önek dizisini 2'şer birer ilerlet ve sonrasında İçindekiler girişi oluşturmak için bir SEQ alanı ekle.
// Önek dizisi artık 2'de ve ana dizi SEQ alanı 3. sayfadadır.
// bu sayede İçindekiler girişi sayfa sayısında "2>3" olarak görüntülenecektir.
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
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
