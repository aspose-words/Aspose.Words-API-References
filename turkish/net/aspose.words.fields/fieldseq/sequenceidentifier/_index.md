---
title: FieldSeq.SequenceIdentifier
linktitle: SequenceIdentifier
articleTitle: SequenceIdentifier
second_title: .NET için Aspose.Words
description: Verimli numaralandırma ve organizasyon için öğe serisi adlarını zahmetsizce yönetmek ve özelleştirmek amacıyla FieldSeq SequenceIdentifier özelliğini keşfedin.
type: docs
weight: 60
url: /tr/net/aspose.words.fields/fieldseq/sequenceidentifier/
---
## FieldSeq.SequenceIdentifier property

Numaralandırılacak öğe serisine atanan adı alır veya ayarlar.

```csharp
public string SequenceIdentifier { get; set; }
```

## Örnekler

SEQ alanlarını kullanarak numaralandırma oluşturmayı gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// SEQ alanları her SEQ alanında artan bir sayım görüntüler.
// Bu alanlar ayrıca her benzersiz adlandırılmış dizi için ayrı sayımları korur
// SEQ alanının "SequenceIdentifier" özelliği ile tanımlanır.
// "MySequence"ın geçerli sayım değerini görüntüleyecek bir SEQ alanı ekleyin,
// "ResetNumber" özelliğini kullanarak 100'e ayarladıktan sonra.
builder.Write("#");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetNumber = "100";
fieldSeq.Update();

Assert.AreEqual(" SEQ  MySequence \\r 100", fieldSeq.GetFieldCode());
Assert.AreEqual("100", fieldSeq.Result);

// Bu dizideki bir sonraki sayıyı başka bir SEQ alanıyla görüntüle.
builder.Write(", #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.Update();

Assert.AreEqual("101", fieldSeq.Result);

// 1. seviye bir başlık ekle.
builder.InsertBreak(BreakType.ParagraphBreak);
builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("This level 1 heading will reset MySequence to 1");
builder.ParagraphFormat.Style = doc.Styles["Normal"];

// Aynı diziden başka bir SEQ alanı ekle ve her başlıkta 1 ile sayımı sıfırlayacak şekilde yapılandır.
builder.Write("\n#");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetHeadingLevel = "1";
fieldSeq.Update();

// Yukarıdaki başlık 1. seviye bir başlık olduğundan, bu dizinin sayısı 1 olarak sıfırlanır.
Assert.AreEqual(" SEQ  MySequence \\s 1", fieldSeq.GetFieldCode());
Assert.AreEqual("1", fieldSeq.Result);

// Bu dizinin bir sonraki sayısına geç.
builder.Write(", #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.InsertNextNumber = true;
fieldSeq.Update();

Assert.AreEqual(" SEQ  MySequence \\n", fieldSeq.GetFieldCode());
Assert.AreEqual("2", fieldSeq.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SEQ.ResetNumbering.docx");
```

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

* class [FieldSeq](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
