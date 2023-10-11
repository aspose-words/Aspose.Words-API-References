---
title: Class FieldToc
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Fields.FieldToc sınıf. TOC alanını uygular.
type: docs
weight: 2530
url: /tr/net/aspose.words.fields/fieldtoc/
---
## FieldToc class

TOC alanını uygular.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Alanlarla Çalışmak](https://docs.aspose.com/words/net/working-with-fields/) dokümantasyon makalesi.

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
| [BookmarkName](../../aspose.words.fields/fieldtoc/bookmarkname/) { get; set; } | Tabloyu oluşturmak için kullanılan belgenin bölümünü işaretleyen yer işaretinin adını alır veya ayarlar. |
| [CaptionlessTableOfFiguresLabel](../../aspose.words.fields/fieldtoc/captionlesstableoffigureslabel/) { get; set; } | Başlığın etiketini ve numarasını içermeyen bir şekiller tablosu oluştururken kullanılan sıra tanımlayıcının adını alır veya ayarlar. |
| [CustomStyles](../../aspose.words.fields/fieldtoc/customstyles/) { get; set; } | Yerleşik başlık stilleri dışındaki stillerin listesini içindekiler tablosuna dahil etmek için alır veya ayarlar. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [EntryIdentifier](../../aspose.words.fields/fieldtoc/entryidentifier/) { get; set; } | Dahil edilen TC alanlarının tür tanımlayıcılarıyla eşleşmesi gereken bir dizeyi alır veya ayarlar. |
| [EntryLevelRange](../../aspose.words.fields/fieldtoc/entrylevelrange/) { get; set; } | Dahil edilecek içindekiler tablosu girişlerinin düzey aralığını alır veya ayarlar. |
| [EntrySeparator](../../aspose.words.fields/fieldtoc/entryseparator/) { get; set; } | Bir girişi ve onun sayfa numarasını ayıran bir karakter dizisini alır veya ayarlar. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Bir alır[`FieldFormat`](../fieldformat/) Alanın formatlamasına yazılı erişim sağlayan nesne. |
| [HeadingLevelRange](../../aspose.words.fields/fieldtoc/headinglevelrange/) { get; set; } | Dahil edilecek başlık düzeyleri aralığını alır veya ayarlar. |
| [HideInWebLayout](../../aspose.words.fields/fieldtoc/hideinweblayout/) { get; set; } | Web düzeni görünümünde sekme liderinin ve sayfa numaralarının gizlenip gizlenmeyeceğini alır veya ayarlar. |
| [InsertHyperlinks](../../aspose.words.fields/fieldtoc/inserthyperlinks/) { get; set; } | İçindekiler tablosu girişlerinin köprü bağlantıları yapılıp yapılmayacağını alır veya ayarlar. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucu yeniden hesaplanmamalıdır). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [PageNumberOmittingLevelRange](../../aspose.words.fields/fieldtoc/pagenumberomittinglevelrange/) { get; set; } | Sayfa numaralarının atlanacağı içindekiler tablosu girişlerinin düzey aralığını alır veya ayarlar. |
| [PrefixedSequenceIdentifier](../../aspose.words.fields/fieldtoc/prefixedsequenceidentifier/) { get; set; } | Girişin sayfa numarasına bir önekin eklenmesi gereken bir sıranın tanımlayıcısını alır veya ayarlar. |
| [PreserveLineBreaks](../../aspose.words.fields/fieldtoc/preservelinebreaks/) { get; set; } | Tablo girişlerinde yeni satır karakterlerinin korunup korunmayacağını alır veya ayarlar. |
| [PreserveTabs](../../aspose.words.fields/fieldtoc/preservetabs/) { get; set; } | Tablo girişleri içindeki sekme girişlerinin korunup korunmayacağını alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcıyı temsil eden düğümü alır. Olabilir`hükümsüz` . |
| [SequenceSeparator](../../aspose.words.fields/fieldtoc/sequenceseparator/) { get; set; } | Sıra numaralarını ve sayfa numaralarını ayırmak için kullanılan karakter sırasını alır veya ayarlar. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| [TableOfFiguresLabel](../../aspose.words.fields/fieldtoc/tableoffigureslabel/) { get; set; } | Şekiller tablosu oluştururken kullanılan sıra tanımlayıcının adını alır veya ayarlar. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Microsoft Word alan türünü alır. |
| [UseParagraphOutlineLevel](../../aspose.words.fields/fieldtoc/useparagraphoutlinelevel/) { get; set; } | Uygulanan paragraf anahat düzeyinin kullanılıp kullanılmayacağını alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Alt alanların hem alan kodu hem de alan sonucu dahil edilir. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [Remove](../../aspose.words.fields/field/remove/)() | Alanı belgeden kaldırır. Alanın hemen ardından bir düğüm döndürür. Alanın sonu, üst düğümünün son child 'si ise, üst paragrafını döndürür. Alan zaten kaldırılmışsa şunu döndürür:`hükümsüz` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Alanın bağlantısını kaldırır. |
| [Update](../../aspose.words.fields/field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa atar. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa atar. |
| [UpdatePageNumbers](../../aspose.words.fields/fieldtoc/updatepagenumbers/)() | Bu içindekiler tablosundaki öğelerin sayfa numaralarını günceller. |

### Notlar

TC alanları tarafından belirtilen girişleri, bunların başlık düzeylerini ve belirtilen stilleri kullanarak bir içindekiler tablosu (bu aynı zamanda şekiller tablosu da olabilir) oluşturur ve bu tabloyu belgede bu yere ekler.

### Örnekler

İçindekiler tablosunun nasıl ekleneceğini ve başlık stillerine göre girdilerle nasıl doldurulacağını gösterir.

```csharp
public void FieldToc()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("MyBookmark");

    // Tüm başlıkları içindekiler tablosunda derleyecek bir TOC alanı ekleyin.
    // Her başlık için bu alan, solda o başlık stilindeki metnin yer aldığı bir satır oluşturacaktır,
    // ve başlığın sağda göründüğü sayfa.
    FieldToc field = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // Yalnızca başlıkları listelemek için BookmarkName özelliğini kullanın
    // "MyBookmark" adındaki bir yer iminin sınırları içinde görünenler.
    field.BookmarkName = "MyBookmark";

    // "Başlık 1" gibi yerleşik başlık stilinin uygulandığı metin başlık olarak sayılacaktır.
    // TOC tarafından başlık olarak alınacak ek stilleri ve TOC seviyelerini bu özellikte adlandırabiliriz.
    field.CustomStyles = "Quote; 6; Intense Quote; 7";

    // Varsayılan olarak, Stiller/TOC düzeyleri CustomStyles özelliğinde virgülle ayrılır,
    // ancak bu özellikte özel bir sınırlayıcı ayarlayabiliriz.
    doc.FieldOptions.CustomTocStyleSeparator = ";";

    // TOC düzeyleri bu aralığın dışında olan başlıkları hariç tutacak şekilde alanı yapılandırın.
    field.HeadingLevelRange = "1-3";

    // TOC, TOC düzeyleri bu aralıkta olan başlıkların sayfa numaralarını görüntülemeyecektir.
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

    // Bu iki başlık "2-5" aralığında olduğundan sayfa numaraları çıkarılacaktır.
    InsertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
    InsertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

    // "Başlık 4" daha önce belirlediğimiz "1-3" aralığının dışında olduğundan bu giriş görünmüyor.
    InsertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

    builder.EndBookmark("MyBookmark");
    builder.Writeln("Paragraph text.");

    // Bu giriş TOC tarafından belirtilen yer iminin dışında olduğundan görünmüyor.
    InsertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

    Assert.AreEqual(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.GetFieldCode());

    field.UpdatePageNumbers();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TOC.docx");
}

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

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)


