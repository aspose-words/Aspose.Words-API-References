---
title: FieldToc.PrefixedSequenceIdentifier
linktitle: PrefixedSequenceIdentifier
articleTitle: PrefixedSequenceIdentifier
second_title: Aspose.Words for .NET
description: FieldToc PrefixedSequenceIdentifier mülk. Girişin sayfa numarasına bir önekin eklenmesi gereken bir sıranın tanımlayıcısını alır veya ayarlar C#'da.
type: docs
weight: 120
url: /tr/net/aspose.words.fields/fieldtoc/prefixedsequenceidentifier/
---
## FieldToc.PrefixedSequenceIdentifier property

Girişin sayfa numarasına bir önekin eklenmesi gereken bir sıranın tanımlayıcısını alır veya ayarlar.

```csharp
public string PrefixedSequenceIdentifier { get; set; }
```

## Örnekler

Bir TOC alanının SEQ alanlarını kullanarak girişlerle nasıl doldurulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir TOC alanı, belgede bulunan her bir SEQ alanı için içindekiler tablosunda bir giriş oluşturabilir.
// Her giriş, SEQ alanını içeren paragrafı ve alanın göründüğü sayfanın numarasını içerir.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// SEQ alanları, her SEQ alanında artan bir sayım görüntüler.
// Bu alanlar ayrıca her benzersiz adlandırılmış dizi için ayrı sayıları korur
// SEQ alanının "SequenceIdentifier" özelliği tarafından tanımlanır.
// TOC'nin ana dizisini adlandırmak için "TableOfFigürlerLabel" özelliğini kullanın.
// Şimdi, bu TOC yalnızca "SequenceIdentifier"ı "MySequence" olarak ayarlanmış SEQ alanlarından girişler oluşturacaktır.
fieldToc.TableOfFiguresLabel = "MySequence";

// "PrefixedSequenceIdentifier" özelliğinde başka bir SEQ alanı dizisine isim verebiliriz.
 // Bu önek dizisindeki SEQ alanları TOC girişleri oluşturmayacaktır.
// Bir ana sıra SEQ alanından oluşturulan her TOC girişi artık aynı zamanda o sayıyı da görüntüleyecektir.
// önek dizisi şu anda girişi yapan birincil dizi SEQ alanında açık.
fieldToc.PrefixedSequenceIdentifier = "PrefixSequence";

// Her TOC girişi, hemen solda önek sırası sayısını görüntüleyecektir
// ana sıra SEQ alanının göründüğü sayfa numarasının.
// Bu iki sayı arasında görünecek özel bir ayırıcı belirtebiliriz.
fieldToc.SequenceSeparator = ">";

Assert.AreEqual(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);

// Bu TOC'yi doldurmak için SEQ alanlarını kullanmanın iki yolu vardır.
// 1 - TOC'nin önek dizisine ait bir SEQ alanı ekleme:
// Bu alan "PrefixSequence" için SEQ dizi sayısını 1 artıracaktır.
// Bu alan tanımlanan ana diziye ait olmadığından
// TOC'un "TableOfFigürlerLabel" özelliği sayesinde girdi olarak gözükmeyecektir.
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();

Assert.AreEqual(" SEQ  PrefixSequence", fieldSeq.GetFieldCode());

// 2 - TOC'nin ana dizisine ait bir SEQ alanı ekleme:
// Bu SEQ alanı TOC'de bir giriş oluşturacaktır.
// TOC girişi SEQ alanının bulunduğu paragrafı ve göründüğü sayfanın numarasını içerecektir.
// Bu giriş aynı zamanda önek dizisinin şu anda bulunduğu sayıyı da gösterecektir,
// TOC'nin SeqenceSeparator özelliğindeki değere göre sayfa numarasından ayrıldı.
// "PrefixSequence" sayısı 1'de, bu ana dizi SEQ alanı 2. sayfada,
// ve ayırıcı ">" olduğundan girişte "1>2" görüntülenecektir.
builder.Write("First TOC entry, MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", fieldSeq.GetFieldCode());

// Bir sayfa ekleyin, önek sırasını 2 birim ilerletin ve daha sonra bir TOC girişi oluşturmak için bir SEQ alanı ekleyin.
// Ön ek dizisi şimdi 2'de ve ana sıra SEQ alanı 3. sayfada,
// böylece TOC girişi sayfa sayısında "2>3" gösterecektir.
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
