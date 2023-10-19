---
title: BookmarksOutlineLevelCollection Class
linktitle: BookmarksOutlineLevelCollection
articleTitle: BookmarksOutlineLevelCollection
second_title: Aspose.Words for .NET
description: Aspose.Words.Saving.BookmarksOutlineLevelCollection sınıf. Bireysel yer imlerinin anahat düzeyinden oluşan bir koleksiyon C#'da.
type: docs
weight: 4850
url: /tr/net/aspose.words.saving/bookmarksoutlinelevelcollection/
---
## BookmarksOutlineLevelCollection class

Bireysel yer imlerinin anahat düzeyinden oluşan bir koleksiyon.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Yer İşaretleriyle Çalışmak](https://docs.aspose.com/words/net/working-with-bookmarks/) dokümantasyon makalesi.

```csharp
public class BookmarksOutlineLevelCollection : IEnumerable<KeyValuePair<string, int>>
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [BookmarksOutlineLevelCollection](bookmarksoutlinelevelcollection/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.saving/bookmarksoutlinelevelcollection/count/) { get; } | Koleksiyonda yer alan öğelerin sayısını alır. |
| [Item](../../aspose.words.saving/bookmarksoutlinelevelcollection/item/) { get; set; } | Yer imi adına göre bir yer imi anahat düzeyini alır veya ayarlar. (2 indexers) |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words.saving/bookmarksoutlinelevelcollection/add/)(*string, int*) | Koleksiyona bir yer işareti ekler. |
| [Clear](../../aspose.words.saving/bookmarksoutlinelevelcollection/clear/)() | Koleksiyondaki tüm öğeleri kaldırır. |
| [Contains](../../aspose.words.saving/bookmarksoutlinelevelcollection/contains/)(*string*) | Koleksiyonun belirtilen adda bir yer işareti içerip içermediğini belirler. |
| [GetEnumerator](../../aspose.words.saving/bookmarksoutlinelevelcollection/getenumerator/)() | Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilecek bir numaralandırıcı nesnesini döndürür. |
| [IndexOfKey](../../aspose.words.saving/bookmarksoutlinelevelcollection/indexofkey/)(*string*) | Koleksiyonda belirtilen yer iminin sıfır tabanlı dizinini döndürür. |
| [Remove](../../aspose.words.saving/bookmarksoutlinelevelcollection/remove/)(*string*) | Koleksiyondan belirtilen ada sahip bir yer işaretini kaldırır. |
| [RemoveAt](../../aspose.words.saving/bookmarksoutlinelevelcollection/removeat/)(*int*) | Belirtilen dizindeki yer imini kaldırır. |

## Notlar

Anahtar, büyük/küçük harfe duyarlı olmayan bir dize yer imi adıdır. Değer, int yer imi anahat düzeyidir.

Yer imi anahat düzeyi 0 ile 9 arasında bir değer olabilir. 0 belirtin; Word yer imi belge anahattında görüntülenmez. 1 belirtin ve Word yer imi belge anahattı içinde düzey 1'de görüntülenecektir; 2. seviye için 2 vb.

## Örnekler

Yer imleri için anahat düzeylerinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// İçine başka bir yer imi yerleştirilmiş bir yer imi ekleyin.
builder.StartBookmark("Bookmark 1");
builder.Writeln("Text inside Bookmark 1.");

builder.StartBookmark("Bookmark 2");
builder.Writeln("Text inside Bookmark 1 and 2.");
builder.EndBookmark("Bookmark 2");

builder.Writeln("Text inside Bookmark 1.");
builder.EndBookmark("Bookmark 1");

// Başka bir yer imi ekleyin.
builder.StartBookmark("Bookmark 3");
builder.Writeln("Text inside Bookmark 3.");
builder.EndBookmark("Bookmark 3");

// .pdf olarak kaydederken, yer imlerine açılır menü aracılığıyla erişilebilir ve çoğu okuyucu tarafından bağlantı noktası olarak kullanılabilir.
// Yer imleri aynı zamanda anahat düzeyleri için sayısal değerlere de sahip olabilir,
// okuyucuda daraltıldığında üst düzey alt girişleri gizlemek için alt düzey anahat girişlerini etkinleştirme.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
BookmarksOutlineLevelCollection outlineLevels = pdfSaveOptions.OutlineOptions.BookmarksOutlineLevels;

outlineLevels.Add("Bookmark 1", 1);
outlineLevels.Add("Bookmark 2", 2);
outlineLevels.Add("Bookmark 3", 3);

Assert.AreEqual(3, outlineLevels.Count);
Assert.True(outlineLevels.Contains("Bookmark 1"));
Assert.AreEqual(1, outlineLevels[0]);
Assert.AreEqual(2, outlineLevels["Bookmark 2"]);
Assert.AreEqual(2, outlineLevels.IndexOfKey("Bookmark 3"));

// İki öğeyi kaldırabiliriz, böylece yalnızca "Yer İşareti 1" için anahat düzeyi ataması kalır.
outlineLevels.RemoveAt(2);
outlineLevels.Remove("Bookmark 2");

// Dokuz anahat düzeyi vardır. Kaydetme işlemi sırasında numaralandırmaları optimize edilecektir.
// Bu durumda "5" ve "9" seviyeleri "2" ve "3" olacaktır.
outlineLevels.Add("Bookmark 2", 5);
outlineLevels.Add("Bookmark 3", 9);

doc.Save(ArtifactsDir + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

// Bu koleksiyonun boşaltılması yer imlerini koruyacak ve hepsini aynı anahat düzeyine koyacaktır.
outlineLevels.Clear();
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
