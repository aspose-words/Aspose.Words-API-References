---
title: Class FieldIndex
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Fields.FieldIndex sınıf. INDEX alanını uygular.
type: docs
weight: 1910
url: /tr/net/aspose.words.fields/fieldindex/
---
## FieldIndex class

INDEX alanını uygular.

```csharp
public class FieldIndex : Field
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FieldIndex](fieldindex/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldindex/bookmarkname/) { get; set; } | Belgenin dizini oluşturmak için kullanılan bölümünü işaretleyen yer iminin adını alır veya ayarlar. |
| [CrossReferenceSeparator](../../aspose.words.fields/fieldindex/crossreferenceseparator/) { get; set; } | Çapraz referansları ve diğer girdileri ayırmak için kullanılan karakter dizisini alır veya ayarlar. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [EntryType](../../aspose.words.fields/fieldindex/entrytype/) { get; set; } | Dizini oluşturmak için kullanılan bir dizin girişi türünü alır veya ayarlar. |
| [Format](../../aspose.words.fields/field/format/) { get; } | [`FieldFormat`](../fieldformat/) alanın biçimlendirmesine yazılı erişim sağlayan nesne. |
| [HasPageNumberSeparator](../../aspose.words.fields/fieldindex/haspagenumberseparator/) { get; } | Alan kodu üzerinden bir sayfa numarası ayırıcısının geçersiz kılınıp kılınmadığını gösteren bir değer alır. |
| [HasSequenceName](../../aspose.words.fields/fieldindex/hassequencename/) { get; } | Alanın sonucu oluşturulurken bir dizinin kullanılması gerekip gerekmediğini gösteren bir değer alır. |
| [Heading](../../aspose.words.fields/fieldindex/heading/) { get; set; } | Herhangi bir harf için her giriş kümesinin başında görünen bir başlık alır veya ayarlar. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [LanguageId](../../aspose.words.fields/fieldindex/languageid/) { get; set; } | Dizini oluşturmak için kullanılan dil kimliğini alır veya ayarlar. |
| [LetterRange](../../aspose.words.fields/fieldindex/letterrange/) { get; set; } | Dizini sınırlayan bir harf aralığı alır veya ayarlar. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [NumberOfColumns](../../aspose.words.fields/fieldindex/numberofcolumns/) { get; set; } | Dizini oluştururken kullanılan sayfa başına sütun sayısını alır veya ayarlar. |
| [PageNumberListSeparator](../../aspose.words.fields/fieldindex/pagenumberlistseparator/) { get; set; } | Bir sayfa numarası listesindeki iki sayfa numarasını ayırmak için kullanılan karakter dizisini alır veya ayarlar. |
| [PageNumberSeparator](../../aspose.words.fields/fieldindex/pagenumberseparator/) { get; set; } | Bir dizin girişi ile sayfa numarasını ayırmak için kullanılan karakter dizisini alır veya ayarlar. |
| [PageRangeSeparator](../../aspose.words.fields/fieldindex/pagerangeseparator/) { get; set; } | Bir sayfa aralığının başlangıcını ve sonunu ayırmak için kullanılan karakter dizisini alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [RunSubentriesOnSameLine](../../aspose.words.fields/fieldindex/runsubentriesonsameline/) { get; set; } | Alt girdilerin ana girdiyle aynı satırda çalıştırılıp çalıştırılmayacağını alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcıyı temsil eden düğümü alır. null. olabilir |
| [SequenceName](../../aspose.words.fields/fieldindex/sequencename/) { get; set; } | Numarası sayfa numarasına dahil olan bir dizinin adını alır veya ayarlar. |
| [SequenceSeparator](../../aspose.words.fields/fieldindex/sequenceseparator/) { get; set; } | Sıra numaralarını ve sayfa numaralarını ayırmak için kullanılan karakter sırasını alır veya ayarlar. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Microsoft Word alan türünü alır. |
| [UseYomi](../../aspose.words.fields/fieldindex/useyomi/) { get; set; } | Dizin girişleri için yomi metni kullanımının etkinleştirilip etkinleştirilmeyeceğini alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Alt alanların hem alan kodu hem de alan sonucu dahil edilir. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [Remove](../../aspose.words.fields/field/remove/)() | Alanı belgeden kaldırır. Alandan hemen sonra bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğu ise, üst paragrafını döndürür. Alan zaten kaldırılmışsa, döner **hükümsüz** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Bağlantıyı kaldır alanını gerçekleştirir. |
| [Update](../../aspose.words.fields/field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa atar. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa atar. |

### Notlar

XE alanları tarafından belirtilen dizin girişlerini kullanarak bir dizin oluşturur ve bu dizini belgede bu yere ekler.

### Örnekler

Bir INDEX alanının nasıl oluşturulacağını ve ardından onu girdilerle doldurmak için XE alanlarının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgede bulunan her XE alanı için bir giriş görüntüleyecek bir INDEX alanı oluşturun.
// Her giriş, XE alanının Metin özellik değerini sol tarafta gösterecek
// ve sağda XE alanını içeren sayfa.
// XE alanları "Text" özelliğinde aynı değere sahipse,
// INDEX alanı bunları tek bir girişte gruplayacaktır.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// INDEX alanını yalnızca sınırlar içindeki XE alanlarını gösterecek şekilde yapılandırın
// "MainBookmark" adlı ve "EntryType" özellikleri "A" değerine sahip bir yer işaretinin.
// Hem INDEX hem de XE alanları için "EntryType" özelliği, dize değerinin yalnızca ilk karakterini kullanır.
index.BookmarkName = "MainBookmark";
index.EntryType = "A";

Assert.AreEqual(" INDEX  \\b MainBookmark \\f A", index.GetFieldCode());

// Yeni bir sayfada, yer imini değerle eşleşen bir adla başlatın
// INDEX alanının "Yer İşaretiAdı" özelliğinin.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("MainBookmark");

// INDEX alanı, yer iminin içinde olduğu için bu girişi alacaktır,
// ve onun giriş tipi de INDEX alanının giriş tipiyle eşleşir.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 1";
indexEntry.EntryType = "A";

Assert.AreEqual(" XE  \"Index entry 1\" \\f A", indexEntry.GetFieldCode());

// Giriş türleri eşleşmediği için INDEX'te görünmeyecek bir XE alanı ekleyin.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 2";
indexEntry.EntryType = "B";

// Yer imini sonlandırın ve ardından bir XE alanı ekleyin.
// INDEX alanıyla aynı türdendir, ancak görünmeyecektir
// yer iminin sınırlarının dışında olduğu için.
builder.EndBookmark("MainBookmark");
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 3";
indexEntry.EntryType = "A";

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Filtering.docx");
```

Bir INDEX alanının XE alanlarını kullanarak girişlerle nasıl doldurulacağını ve görünümünün nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgede bulunan her XE alanı için bir giriş görüntüleyecek bir INDEX alanı oluşturun.
// Her giriş, sol tarafta XE alanının Text özellik değerini gösterecek,
// ve sağdaki XE alanını içeren sayfanın numarası.
// XE alanları "Text" özelliğinde aynı değere sahipse,
// INDEX alanı bunları tek bir girişte gruplayacaktır.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.LanguageId = "1033";

// Bu özelliğin değerini "A" olarak ayarlamak, tüm girişleri ilk harflerine göre gruplayacaktır,
// ve o harfi her grubun üstüne büyük harfle yerleştirin.
index.Heading = "A";

// INDEX alanı tarafından oluşturulan tabloyu 2 sütuna yayılacak şekilde ayarlayın.
index.NumberOfColumns = "2";

// "ac" karakter aralığının dışında başlangıç harfleri olan tüm girişleri atlanacak şekilde ayarlayın.
index.LetterRange = "a-c";

Assert.AreEqual(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.GetFieldCode());

// Sonraki iki XE alanı "A" başlığının altında görünecek,
// sayfa numaralarına da uygulanmış ilgili metin stilleriyle.
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apple";
indexEntry.IsItalic = true;

Assert.AreEqual(" XE  Apple \\i", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apricot";
indexEntry.IsBold = true;

Assert.AreEqual(" XE  Apricot \\b", indexEntry.GetFieldCode());

// Sonraki iki XE alanının her ikisi de INDEX alanları içindekiler tablosunda "B" ve "C" başlığı altında olacaktır.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Banana";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cherry";

// INDEX alanları tüm girdileri alfabetik olarak sıralar, bu nedenle bu girdi diğer ikisi ile birlikte "A" altında görünecektir.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Avocado";

// Bu girdi "D" harfiyle başladığı için görünmeyecek,
// INDEX alanının LetterRange özelliğinin tanımladığı "ac" karakter aralığının dışında olan.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Durian";

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Formatting.docx");
```

### Ayrıca bakınız

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)


