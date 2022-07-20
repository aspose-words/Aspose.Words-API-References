---
title: FieldSeq
second_title: Aspose.Words for .NET API Referansı
description: SEQ alanını uygular.
type: docs
weight: 2240
url: /tr/net/aspose.words.fields/fieldseq/
---
## FieldSeq class

SEQ alanını uygular.

```csharp
public class FieldSeq : Field
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FieldSeq](fieldseq)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldseq/bookmarkname) { get; set; } | Geçerli konum yerine belgenin başka bir yerindeki bir öğeye başvuran bir yer imi adı alır veya ayarlar. |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [End](../../aspose.words.fields/field/end) { get; } | Alan sonunu temsil eden düğümü alır. |
| [Format](../../aspose.words.fields/field/format) { get; } | [`FieldFormat`](../fieldformat) alanın biçimlendirmesine yazılı erişim sağlayan nesne. |
| [InsertNextNumber](../../aspose.words.fields/fieldseq/insertnextnumber) { get; set; } | Belirtilen öğe için sonraki sıra numarasının eklenip eklenmeyeceğini alır veya ayarlar. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [ResetHeadingLevel](../../aspose.words.fields/fieldseq/resetheadinglevel) { get; set; } | Sıra numarasını sıfırlamak için bir başlık düzeyini temsil eden bir tamsayı alır veya ayarlar. Sayı yoksa -1 döndürür. |
| [ResetNumber](../../aspose.words.fields/fieldseq/resetnumber) { get; set; } | Sıra numarasını sıfırlamak için bir tamsayı alır veya ayarlar. Sayı yoksa -1 döndürür. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Alan ayırıcıyı temsil eden düğümü alır. null. olabilir |
| [SequenceIdentifier](../../aspose.words.fields/fieldseq/sequenceidentifier) { get; set; } | Numaralandırılacak öğe serisine atanan adı alır veya ayarlar. |
| [Start](../../aspose.words.fields/field/start) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Microsoft Word alan türünü alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Alt alanların hem alan kodu hem de alan sonucu dahil edilir. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [Remove](../../aspose.words.fields/field/remove)() | Alanı belgeden kaldırır. Alandan hemen sonra bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğu ise, üst paragrafını döndürür. Alan zaten kaldırılmışsa, döner **hükümsüz** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | Bağlantıyı kaldır alanını gerçekleştirir. |
| [Update](../../aspose.words.fields/field/update)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa atar. |
| [Update](../../aspose.words.fields/field/update)(bool) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa atar. |

### Notlar

Bir belgedeki bölümleri, tabloları, şekilleri ve diğer kullanıcı tanımlı öğe listelerini sırayla numaralandırır.

### Örnekler

SEQ alanlarını kullanarak numaralandırma oluşturmayı gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// SEQ alanları, her SEQ alanında artan bir sayı görüntüler.
// Bu alanlar ayrıca her benzersiz adlandırılmış dizi için ayrı sayılar tutar
// SEQ alanının "SequenceIdentifier" özelliği ile tanımlanır.
// "MySequence"ın geçerli sayım değerini gösterecek bir SEQ alanı ekleyin,
// 100'e ayarlamak için "ResetNumber" özelliğini kullandıktan sonra.
builder.Write("#");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetNumber = "100";
fieldSeq.Update();

Assert.AreEqual(" SEQ  MySequence \\r 100", fieldSeq.GetFieldCode());
Assert.AreEqual("100", fieldSeq.Result);

// Bu dizideki bir sonraki sayıyı başka bir SEQ alanı ile göster.
builder.Write(", #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.Update();

Assert.AreEqual("101", fieldSeq.Result);

// 1. düzey bir başlık girin.
builder.InsertBreak(BreakType.ParagraphBreak);
builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("This level 1 heading will reset MySequence to 1");
builder.ParagraphFormat.Style = doc.Styles["Normal"];

// Aynı diziden başka bir SEQ alanı ekleyin ve her başlıktaki sayımı 1 ile sıfırlayacak şekilde yapılandırın.
builder.Write("\n#");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetHeadingLevel = "1";
fieldSeq.Update();

// Yukarıdaki başlık 1. seviye başlıktır, bu nedenle bu dizinin sayısı 1'e sıfırlanır.
Assert.AreEqual(" SEQ  MySequence \\s 1", fieldSeq.GetFieldCode());
Assert.AreEqual("1", fieldSeq.Result);

// Bu dizinin bir sonraki numarasına git.
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

İçindekiler ve sıra alanlarının nasıl birleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir TOC alanı, belgede bulunan her SEQ alanı için içindekiler tablosunda bir giriş oluşturabilir.
// Her giriş, SEQ alanını içeren paragrafı içerir,
// ve alanın göründüğü sayfanın numarası.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// Bu TOC alanını, "MySequence" değerine sahip bir SequenceIdentifier özelliğine sahip olacak şekilde yapılandırın.
fieldToc.TableOfFiguresLabel = "MySequence";

// Bu TOC alanını yalnızca bir yer iminin sınırları içindeki SEQ alanlarını alacak şekilde yapılandırın
// "TOCBookmark" olarak adlandırıldı.
fieldToc.BookmarkName = "TOCBookmark";
builder.InsertBreak(BreakType.PageBreak);

Assert.AreEqual(" TOC  \\c MySequence \\b TOCBookmark", fieldToc.GetFieldCode());

// SEQ alanları, her SEQ alanında artan bir sayı görüntüler.
// Bu alanlar ayrıca her benzersiz adlandırılmış dizi için ayrı sayılar tutar
// SEQ alanının "SequenceIdentifier" özelliği ile tanımlanır.
// İçindekiler ile eşleşen bir dizi tanımlayıcıya sahip bir SEQ alanı ekleyin
// TableOf FiguresLabel özelliği. Bu alan, dışarıda olduğu için TOC'de bir giriş oluşturmaz.
// "Yer İşaretiAdı" tarafından belirlenen yer işaretinin sınırları.
builder.Write("MySequence #");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will not show up in the TOC because it is outside of the bookmark.");

builder.StartBookmark("TOCBookmark");

// Bu SEQ alanının sırası, İçindekiler'in "TableOf FiguresLabel" özelliğiyle eşleşir ve yer iminin sınırları içindedir.
// Bu alanı içeren paragraf, TOC'de bir giriş olarak görünecektir.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will show up in the TOC next to the entry for the above caption.");

// Bu SEQ alanının sırası, İçindekiler'in "TableOf FiguresLabel" özelliğiyle eşleşmiyor,
// ve yer iminin sınırları içinde. Paragrafı TOC'de bir giriş olarak görünmeyecektir.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "OtherSequence";
builder.Writeln(", will not show up in the TOC because it's from a different sequence identifier.");

// Bu SEQ alanının sırası, İçindekiler'in "TableOf FiguresLabel" özelliğiyle eşleşir ve yer iminin sınırları içindedir.
// Bu alan aynı zamanda başka bir yer işaretine de referansta bulunur. Bu yer iminin içeriği, bu SEQ alanı için TOC girişinde görünecektir.
// SEQ alanının kendisi o yer iminin içeriğini göstermeyecektir.
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.BookmarkName = "SEQBookmark";
Assert.AreEqual(" SEQ  MySequence SEQBookmark", fieldSeq.GetFieldCode());

// Yukarıdaki SEQ alanı referans aldığı için TOC girişinde görünecek içeriğe sahip bir yer imi oluşturun.
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

* class [Field](../field)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
