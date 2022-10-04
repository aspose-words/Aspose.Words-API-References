---
title: FieldToc
second_title: Aspose.Words for .NET API Referansı
description: İçindekiler alanını uygular.
type: docs
weight: 2380
url: /tr/net/aspose.words.fields/fieldtoc/
---
## FieldToc class

İçindekiler alanını uygular.

```csharp
public class FieldToc : Field
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FieldToc](fieldtoc/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldtoc/bookmarkname/) { get; set; } | Belgenin tabloyu oluşturmak için kullanılan bölümünü işaretleyen yer iminin adını alır veya ayarlar. |
| [CaptionlessTableOfFiguresLabel](../../aspose.words.fields/fieldtoc/captionlesstableoffigureslabel/) { get; set; } | Resim yazısının etiketini ve numarasını içermeyen bir şekil tablosu oluştururken kullanılan sıra tanımlayıcısının adını alır veya ayarlar. |
| [CustomStyles](../../aspose.words.fields/fieldtoc/customstyles/) { get; set; } | İçindekiler tablosuna dahil edilecek yerleşik başlık stilleri dışındaki stillerin bir listesini alır veya ayarlar. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [EntryIdentifier](../../aspose.words.fields/fieldtoc/entryidentifier/) { get; set; } | Dahil edilen TC alanlarının tür tanımlayıcılarıyla eşleşmesi gereken bir dize alır veya ayarlar. |
| [EntryLevelRange](../../aspose.words.fields/fieldtoc/entrylevelrange/) { get; set; } | Dahil edilecek içindekiler tablosu girişlerinin bir dizi düzeyini alır veya ayarlar. |
| [EntrySeparator](../../aspose.words.fields/fieldtoc/entryseparator/) { get; set; } | Bir girdi ile sayfa numarasını ayıran bir karakter dizisini alır veya ayarlar. |
| [Format](../../aspose.words.fields/field/format/) { get; } | [`FieldFormat`](../fieldformat/) alanın biçimlendirmesine yazılı erişim sağlayan nesne. |
| [HeadingLevelRange](../../aspose.words.fields/fieldtoc/headinglevelrange/) { get; set; } | Dahil edilecek bir dizi başlık düzeyi alır veya ayarlar. |
| [HideInWebLayout](../../aspose.words.fields/fieldtoc/hideinweblayout/) { get; set; } | Web düzeni görünümünde sekme öncüsü ve sayfa numaralarının gizlenip gizlenmeyeceğini alır veya ayarlar. |
| [InsertHyperlinks](../../aspose.words.fields/fieldtoc/inserthyperlinks/) { get; set; } | İçindekiler girişlerinin köprüler yapılıp yapılmayacağını alır veya ayarlar. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [PageNumberOmittingLevelRange](../../aspose.words.fields/fieldtoc/pagenumberomittinglevelrange/) { get; set; } | Sayfa numaralarının çıkarılacağı içindekiler tablosu girişlerinin bir dizi düzeyini alır veya ayarlar. |
| [PrefixedSequenceIdentifier](../../aspose.words.fields/fieldtoc/prefixedsequenceidentifier/) { get; set; } | Girdinin sayfa numarasına bir önek eklenmesi gereken bir dizinin tanımlayıcısını alır veya ayarlar. |
| [PreserveLineBreaks](../../aspose.words.fields/fieldtoc/preservelinebreaks/) { get; set; } | Tablo girişlerinde yeni satır karakterlerinin korunup korunmayacağını alır veya ayarlar. |
| [PreserveTabs](../../aspose.words.fields/fieldtoc/preservetabs/) { get; set; } | Tablo girişlerinde sekme girişlerinin korunup korunmayacağını alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcıyı temsil eden düğümü alır. null. olabilir |
| [SequenceSeparator](../../aspose.words.fields/fieldtoc/sequenceseparator/) { get; set; } | Sıra numaralarını ve sayfa numaralarını ayırmak için kullanılan karakter sırasını alır veya ayarlar. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| [TableOfFiguresLabel](../../aspose.words.fields/fieldtoc/tableoffigureslabel/) { get; set; } | Bir şekil tablosu oluştururken kullanılan dizi tanımlayıcısının adını alır veya ayarlar. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Microsoft Word alan türünü alır. |
| [UseParagraphOutlineLevel](../../aspose.words.fields/fieldtoc/useparagraphoutlinelevel/) { get; set; } | Uygulanan paragraf anahat düzeyinin kullanılıp kullanılmayacağını alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Alt alanların hem alan kodu hem de alan sonucu dahil edilir. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [Remove](../../aspose.words.fields/field/remove/)() | Alanı belgeden kaldırır. Alandan hemen sonra bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğu ise, üst paragrafını döndürür. Alan zaten kaldırılmışsa, döner **hükümsüz** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Bağlantıyı kaldır alanını gerçekleştirir. |
| [Update](../../aspose.words.fields/field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa atar. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa atar. |
| [UpdatePageNumbers](../../aspose.words.fields/fieldtoc/updatepagenumbers/)() | Bu içindekiler tablosundaki öğelerin sayfa numaralarını günceller. |

### Notlar

TC alanları, başlık düzeyleri ve belirtilen stiller tarafından belirtilen girişleri kullanarak bir içindekiler tablosu (şekil tablosu da olabilir) oluşturur ve bu tabloyu belgede bu yere ekler.

### Örnekler

İçindekiler'in nasıl ekleneceğini ve başlık stillerine göre girişlerle nasıl doldurulacağını gösterir.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("MyBookmark");

    // Tüm başlıkları bir içindekiler tablosunda derleyecek bir TOC alanı ekleyin.
    // Her başlık için bu alan, soldaki o başlık stilindeki metinle birlikte bir satır oluşturacaktır,
    // ve başlığın sağda göründüğü sayfa.
    FieldToc field = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // Yalnızca başlıkları listelemek için BookmarkName özelliğini kullanın
    // "MyBookmark" adıyla bir yer iminin sınırları içinde görünen.
    field.BookmarkName = "MyBookmark";

    // "Başlık 1" gibi yerleşik bir başlık stiline sahip metinler, başlık olarak sayılır.
    // Bu özellikte TOC tarafından başlık olarak alınacak ek stilleri ve TOC seviyelerini adlandırabiliriz.
    field.CustomStyles = "Quote; 6; Intense Quote; 7";

    // Varsayılan olarak, Styles/TOC seviyeleri CustomStyles özelliğinde virgülle ayrılır,
    // ancak bu özellikte özel bir sınırlayıcı ayarlayabiliriz.
    doc.FieldOptions.CustomTocStyleSeparator = ";";

    // Bu aralığın dışında TOC düzeylerine sahip tüm başlıkları hariç tutmak için alanı yapılandırın.
    field.HeadingLevelRange = "1-3";

    // İçindekiler, TOC seviyeleri bu aralıkta olan başlıkların sayfa numaralarını göstermeyecektir.
    field.PageNumberOmittingLevelRange = "2-5";

     // Her başlığı sayfa numarasından ayıracak özel bir dize ayarlayın.
    field.EntrySeparator = "-";
    field.InsertHyperlinks = true;
    field.HideInWebLayout = false;
    field.PreserveLineBreaks = true;
    field.PreserveTabs = true;
    field.UseParagraphOutlineLevel = false;

    InsertNewPageWithHeading(builder, "First entry", "Heading 1");
    builder.Writeln("Paragraph text.");
    InsertNewPageWithHeading(builder, "Second entry", "Heading 1");
    InsertNewPageWithHeading(builder, "Third entry", "Quote");
    InsertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

    // Bu iki başlık, "2-5" aralığında oldukları için sayfa numaralarına sahip olmayacaktır.
    InsertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
    InsertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

    // "Başlık 4", daha önce belirlediğimiz "1-3" aralığının dışında olduğu için bu giriş görünmüyor.
    InsertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

    builder.EndBookmark("MyBookmark");
    builder.Writeln("Paragraph text.");

    // Bu girdi, İçindekiler tarafından belirtilen yer iminin dışında olduğu için görünmüyor.
    InsertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

    Assert.AreEqual(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.GetFieldCode());

    field.UpdatePageNumbers();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TOC.docx");

/// <summary>
/// Yeni bir sayfa başlatın ve belirtilen stilde bir paragraf ekleyin.
/// </summary>
public void InsertNewPageWithHeading(DocumentBuilder builder, string captionText, string styleName)
{
    builder.InsertBreak(BreakType.PageBreak);
    string originalStyle = builder.ParagraphFormat.StyleName;
    builder.ParagraphFormat.Style = builder.Document.Styles[styleName];
    builder.Writeln(captionText);
    builder.ParagraphFormat.Style = builder.Document.Styles[originalStyle];
}
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

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
