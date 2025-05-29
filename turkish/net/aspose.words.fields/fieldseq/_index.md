---
title: FieldSeq Class
linktitle: FieldSeq
articleTitle: FieldSeq
second_title: .NET için Aspose.Words
description: Kusursuz SEQ alan uygulaması için Aspose.Words.Fields.FieldSeq sınıfını keşfedin. Güçlü özellikler ve esneklikle belge otomasyonunuzu geliştirin.
type: docs
weight: 2800
url: /tr/net/aspose.words.fields/fieldseq/
---
## FieldSeq class

SEQ alanını uygular.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Alanlarla Çalışma](https://docs.aspose.com/words/net/working-with-fields/) belgeleme makalesi.

```csharp
public class FieldSeq : Field
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FieldSeq](fieldseq/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldseq/bookmarkname/) { get; set; } | Geçerli konumdan ziyade belgenin başka bir yerindeki bir öğeye atıfta bulunan bir yer imi adını alır veya ayarlar. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Bir tane alır[`FieldFormat`](../fieldformat/)alanın biçimlendirmesine yazılmış erişim sağlayan nesne. |
| [InsertNextNumber](../../aspose.words.fields/fieldseq/insertnextnumber/) { get; set; } | Belirtilen öğe için bir sonraki sıra numarasının eklenip eklenmeyeceğini alır veya ayarlar. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [ResetHeadingLevel](../../aspose.words.fields/fieldseq/resetheadinglevel/) { get; set; } | Sıra numarasını sıfırlamak için başlık seviyesini temsil eden bir tam sayı alır veya ayarlar. Sayı yoksa -1 döndürür. |
| [ResetNumber](../../aspose.words.fields/fieldseq/resetnumber/) { get; set; } | Sıra numarasını sıfırlamak için bir tam sayı alır veya ayarlar. Sayı yoksa -1 döndürür. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcısı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcısını temsil eden düğümü alır.`hükümsüz` . |
| [SequenceIdentifier](../../aspose.words.fields/fieldseq/sequenceidentifier/) { get; set; } | Numaralandırılacak öğe serisine atanan adı alır veya ayarlar. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Microsoft Word alan türünü alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcısı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Hem alan kodu hem de alt alanların alan sonucu dahil edilir. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Alan başlangıcı ile alan ayırıcısı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [Remove](../../aspose.words.fields/field/remove/)() | Alanı belgeden kaldırır. Alanın hemen ardından bir düğüm döndürür. Alanın sonu, üst düğümünün son alt 'siyse, üst paragrafını döndürür. Alan zaten kaldırılmışsa, şunu döndürür`hükümsüz` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Alan bağlantısını kaldırma işlemini gerçekleştirir. |
| [Update](../../aspose.words.fields/field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa fırlatır. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa fırlatır. |

## Notlar

Bir belgedeki bölümleri, tabloları, şekilleri ve diğer kullanıcı tanımlı öğe listelerini sıralı olarak numaralandırır.

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

İçindekiler tablosu ve sıra alanlarının nasıl birleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir TOC alanı, belgede bulunan her SEQ alanı için içerik tablosunda bir giriş oluşturabilir.
// Her giriş, SEQ alanını içeren paragrafı içerir.
// ve alanın göründüğü sayfanın numarası.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// Bu TOC alanını "MySequence" değerine sahip bir SequenceIdentifier özelliğine sahip olacak şekilde yapılandırın.
fieldToc.TableOfFiguresLabel = "MySequence";

// Bu TOC alanını yalnızca bir yer imi sınırları içindeki SEQ alanlarını alacak şekilde yapılandırın
// "TOCBookmark" olarak adlandırıldı.
fieldToc.BookmarkName = "TOCBookmark";
builder.InsertBreak(BreakType.PageBreak);

Assert.AreEqual(" TOC  \\c MySequence \\b TOCBookmark", fieldToc.GetFieldCode());

// SEQ alanları her SEQ alanında artan bir sayım görüntüler.
// Bu alanlar ayrıca her benzersiz adlandırılmış dizi için ayrı sayımları korur
// SEQ alanının "SequenceIdentifier" özelliği ile tanımlanır.
// İçindekiler tablosuyla eşleşen bir dizi tanımlayıcısına sahip bir SEQ alanı ekleyin
// TableOfFiguresLabel özelliği. Bu alan, TOC'de bir giriş oluşturmaz çünkü dışarıdadır
// "BookmarkName" ile belirtilen yer iminin sınırları.
builder.Write("MySequence #");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will not show up in the TOC because it is outside of the bookmark.");

builder.StartBookmark("TOCBookmark");

// Bu SEQ alanının dizisi, TOC'nin "TableOfFiguresLabel" özelliğiyle eşleşiyor ve yer iminin sınırları içinde.
// Bu alanı içeren paragraf, İçindekiler tablosunda bir giriş olarak gösterilecektir.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will show up in the TOC next to the entry for the above caption.");

// Bu SEQ alanının dizisi TOC'nin "TableOfFiguresLabel" özelliğiyle eşleşmiyor,
// ve yer iminin sınırları içindedir. Paragrafı TOC'de bir giriş olarak görünmeyecektir.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "OtherSequence";
builder.Writeln(", will not show up in the TOC because it's from a different sequence identifier.");

// Bu SEQ alanının dizisi, TOC'nin "TableOfFiguresLabel" özelliğiyle eşleşiyor ve yer iminin sınırları içinde.
// Bu alan başka bir yer imine de başvurur. Bu yer iminin içerikleri bu SEQ alanının TOC girişinde görünecektir.
// SEQ alanı, söz konusu yer iminin içeriğini görüntülemeyecektir.
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.BookmarkName = "SEQBookmark";
Assert.AreEqual(" SEQ  MySequence SEQBookmark", fieldSeq.GetFieldCode());

// Yukarıdaki SEQ alanının referans vermesi nedeniyle TOC girişinde gösterilecek içeriklere sahip bir yer imi oluşturun.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("SEQBookmark");
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", text from inside SEQBookmark.");
builder.EndBookmark("SEQBookmark");

builder.EndBookmark("TOCBookmark");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SEQ.Bookmark.docx");
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

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
