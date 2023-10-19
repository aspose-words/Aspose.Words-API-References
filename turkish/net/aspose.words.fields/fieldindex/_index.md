---
title: FieldIndex Class
linktitle: FieldIndex
articleTitle: FieldIndex
second_title: Aspose.Words for .NET
description: Aspose.Words.Fields.FieldIndex sınıf. INDEX alanını uygular C#'da.
type: docs
weight: 2060
url: /tr/net/aspose.words.fields/fieldindex/
---
## FieldIndex class

INDEX alanını uygular.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Alanlarla Çalışmak](https://docs.aspose.com/words/net/working-with-fields/) dokümantasyon makalesi.

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
| [BookmarkName](../../aspose.words.fields/fieldindex/bookmarkname/) { get; set; } | Dizini oluşturmak için kullanılan belgenin bölümünü işaretleyen yer işaretinin adını alır veya ayarlar. |
| [CrossReferenceSeparator](../../aspose.words.fields/fieldindex/crossreferenceseparator/) { get; set; } | Çapraz referansları ve diğer girişleri ayırmak için kullanılan karakter dizisini alır veya ayarlar. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [EntryType](../../aspose.words.fields/fieldindex/entrytype/) { get; set; } | Dizini oluşturmak için kullanılan dizin giriş türünü alır veya ayarlar. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Bir alır[`FieldFormat`](../fieldformat/) Alanın formatlamasına yazılı erişim sağlayan nesne. |
| [HasPageNumberSeparator](../../aspose.words.fields/fieldindex/haspagenumberseparator/) { get; } | Alanın kodu aracılığıyla sayfa numarası ayırıcısının geçersiz kılınıp kılınmadığını belirten bir değer alır. |
| [HasSequenceName](../../aspose.words.fields/fieldindex/hassequencename/) { get; } | Alanın sonuç oluşturulurken bir sıranın kullanılıp kullanılmayacağını belirten bir değer alır. |
| [Heading](../../aspose.words.fields/fieldindex/heading/) { get; set; } | Verilen herhangi bir harf için her giriş kümesinin başında görünen başlığı alır veya ayarlar. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucu yeniden hesaplanmamalıdır). |
| [LanguageId](../../aspose.words.fields/fieldindex/languageid/) { get; set; } | Dizini oluşturmak için kullanılan dil kimliğini alır veya ayarlar. |
| [LetterRange](../../aspose.words.fields/fieldindex/letterrange/) { get; set; } | Dizini sınırlayan harf aralığını alır veya ayarlar. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [NumberOfColumns](../../aspose.words.fields/fieldindex/numberofcolumns/) { get; set; } | Dizini oluştururken sayfa başına kullanılan sütun sayısını alır veya ayarlar. |
| [PageNumberListSeparator](../../aspose.words.fields/fieldindex/pagenumberlistseparator/) { get; set; } | Sayfa numarası listesindeki iki sayfa numarasını ayırmak için kullanılan karakter sırasını alır veya ayarlar. |
| [PageNumberSeparator](../../aspose.words.fields/fieldindex/pagenumberseparator/) { get; set; } | Bir dizin girişini ve onun sayfa numarasını ayırmak için kullanılan karakter sırasını alır veya ayarlar. |
| [PageRangeSeparator](../../aspose.words.fields/fieldindex/pagerangeseparator/) { get; set; } | Sayfa aralığının başlangıcını ve sonunu ayırmak için kullanılan karakter sırasını alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [RunSubentriesOnSameLine](../../aspose.words.fields/fieldindex/runsubentriesonsameline/) { get; set; } | Alt girişlerin ana girişle aynı satırda çalıştırılıp çalıştırılmayacağını alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcıyı temsil eden düğümü alır. Olabilir`hükümsüz` . |
| [SequenceName](../../aspose.words.fields/fieldindex/sequencename/) { get; set; } | Numarası sayfa numarasına dahil edilen bir dizinin adını alır veya ayarlar. |
| [SequenceSeparator](../../aspose.words.fields/fieldindex/sequenceseparator/) { get; set; } | Sıra numaralarını ve sayfa numaralarını ayırmak için kullanılan karakter sırasını alır veya ayarlar. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Microsoft Word alan türünü alır. |
| [UseYomi](../../aspose.words.fields/fieldindex/useyomi/) { get; set; } | Dizin girişleri için yomi metni kullanımının etkinleştirilip etkinleştirilmeyeceğini alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Alt alanların hem alan kodu hem de alan sonucu dahil edilir. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [Remove](../../aspose.words.fields/field/remove/)() | Alanı belgeden kaldırır. Alanın hemen ardından bir düğüm döndürür. Alanın sonu, üst düğümünün son child 'si ise, üst paragrafını döndürür. Alan zaten kaldırılmışsa şunu döndürür:`hükümsüz` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Alanın bağlantısını kaldırır. |
| [Update](../../aspose.words.fields/field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa atar. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa atar. |

## Notlar

XE alanları tarafından belirtilen dizin girişlerini kullanarak bir dizin oluşturur ve bu dizini belgedeki bu yere ekler.

## Örnekler

Bir INDEX alanının nasıl oluşturulacağını ve ardından onu girişlerle doldurmak için XE alanlarının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgede bulunan her XE alanı için bir giriş görüntüleyecek bir INDEX alanı oluşturun.
// Her girişte XE alanının Text özelliği değeri sol tarafta görüntülenecektir
// ve sağda XE alanını içeren sayfa.
// XE alanlarının "Text" özelliğinde aynı değer varsa,
// INDEX alanı bunları tek bir girişte gruplandıracaktır.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// INDEX alanını yalnızca sınırlar içindeki XE alanlarını görüntüleyecek şekilde yapılandırın
// "MainBookmark" adlı ve "EntryType" özellikleri "A" değerine sahip olan bir yer işaretinin.
// Hem INDEX hem de XE alanları için "EntryType" özelliği dize değerinin yalnızca ilk karakterini kullanır.
index.BookmarkName = "MainBookmark";
index.EntryType = "A";

Assert.AreEqual(" INDEX  \\b MainBookmark \\f A", index.GetFieldCode());

// Yeni bir sayfada yer imini değerle eşleşen bir adla başlatın
// INDEX alanının "BookmarkName" özelliğinin.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("MainBookmark");

// INDEX alanı bu girişi alacaktır çünkü bu yer iminin içindedir,
// ve giriş türü aynı zamanda INDEX alanının giriş türüyle de eşleşir.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 1";
indexEntry.EntryType = "A";

Assert.AreEqual(" XE  \"Index entry 1\" \\f A", indexEntry.GetFieldCode());

// Giriş türleri eşleşmediğinden INDEX'te görünmeyecek bir XE alanı ekleyin.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 2";
indexEntry.EntryType = "B";

// Yer imini sonlandırın ve ardından bir XE alanı ekleyin.
// INDEX alanıyla aynı türdedir ancak görünmez
// yer iminin sınırlarının dışında olduğundan.
builder.EndBookmark("MainBookmark");
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 3";
indexEntry.EntryType = "A";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Filtering.docx");
```

Bir INDEX alanının XE alanlarını kullanarak girişlerle nasıl doldurulacağını ve ayrıca görünümünün nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgede bulunan her XE alanı için bir giriş görüntüleyecek bir INDEX alanı oluşturun.
// Her girişte XE alanının Text özelliği değeri sol tarafta görüntülenecektir,
// ve sağdaki XE alanını içeren sayfanın numarası.
// XE alanlarının "Text" özelliğinde aynı değer varsa,
// INDEX alanı bunları tek bir girişte gruplandıracaktır.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.LanguageId = "1033";

// Bu özelliğin değerini "A" olarak ayarlamak tüm girişleri ilk harflerine göre gruplandıracaktır,
// ve o harfi her grubun üstüne büyük harfle yerleştir.
index.Heading = "A";

// INDEX alanı tarafından oluşturulan tabloyu 2 sütuna yayılacak şekilde ayarlayın.
index.NumberOfColumns = "2";

// "ac" karakter aralığının dışında kalan başlangıç harflerine sahip tüm girişleri atlanacak şekilde ayarlayın.
index.LetterRange = "a-c";

Assert.AreEqual(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.GetFieldCode());

// Sonraki iki XE alanı "A" başlığı altında görünecek,
// ilgili metin stilleri sayfa numaralarına da uygulanır.
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

// INDEX alanları tüm girişleri alfabetik olarak sıralar, böylece bu giriş diğer ikisiyle birlikte "A" altında görünecektir.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Avocado";

// Bu girdi "D" harfiyle başladığı için görünmeyecektir,
// INDEX alanının LetterRange özelliğinin tanımladığı "ac" karakter aralığının dışındadır.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Durian";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Formatting.docx");
```

### Ayrıca bakınız

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
