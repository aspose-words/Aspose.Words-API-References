---
title: BookmarksOutlineLevelCollection Class
linktitle: BookmarksOutlineLevelCollection
articleTitle: BookmarksOutlineLevelCollection
second_title: .NET için Aspose.Words
description: Yer imlerini yönetmek ve belge gezintisini zahmetsizce geliştirmek için güçlü bir araç olan Aspose.Words.Saving.BookmarksOutlineLevelCollection sınıfını keşfedin.
type: docs
weight: 5590
url: /tr/net/aspose.words.saving/bookmarksoutlinelevelcollection/
---
## BookmarksOutlineLevelCollection class

Ayrı ayrı yer imleri anahat düzeyi koleksiyonu.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Yer İşaretleriyle Çalışma](https://docs.aspose.com/words/net/working-with-bookmarks/) belgeleme makalesi.

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
| [Count](../../aspose.words.saving/bookmarksoutlinelevelcollection/count/) { get; } | Koleksiyonda bulunan öğelerin sayısını alır. |
| [Item](../../aspose.words.saving/bookmarksoutlinelevelcollection/item/) { get; set; } | Yer imi adına göre bir yer imi anahat düzeyi alır veya ayarlar. (2 indexers) |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words.saving/bookmarksoutlinelevelcollection/add/)(*string, int*) | Koleksiyona bir yer imi ekler. |
| [Clear](../../aspose.words.saving/bookmarksoutlinelevelcollection/clear/)() | Koleksiyondaki tüm öğeleri kaldırır. |
| [Contains](../../aspose.words.saving/bookmarksoutlinelevelcollection/contains/)(*string*) | Koleksiyonun belirtilen ada sahip bir yer imi içerip içermediğini belirler. |
| [GetEnumerator](../../aspose.words.saving/bookmarksoutlinelevelcollection/getenumerator/)() | Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilen bir numaratör nesnesi döndürür. |
| [IndexOfKey](../../aspose.words.saving/bookmarksoutlinelevelcollection/indexofkey/)(*string*) | Koleksiyondaki belirtilen yer iminin sıfır tabanlı dizinini döndürür. |
| [Remove](../../aspose.words.saving/bookmarksoutlinelevelcollection/remove/)(*string*) | Belirtilen ada sahip bir yer imini koleksiyondan kaldırır. |
| [RemoveAt](../../aspose.words.saving/bookmarksoutlinelevelcollection/removeat/)(*int*) | Belirtilen dizindeki bir yer işaretini kaldırır. |

## Notlar

Anahtar, büyük/küçük harfe duyarlı olmayan bir dize yer imi adıdır. Değer, bir int yer imi anahat düzeyidir.

Yer imi anahat düzeyi 0 ile 9 arasında bir değer olabilir. 0 belirtin ve Word yer imi belge anahattında görüntülenmeyecektir. 1 belirtin ve Word yer imi belge anahattında düzey 1'de; düzey 2 için 2 vb. görüntülenecektir.

## Örnekler

Yer imleri için anahat düzeylerinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// İçerisine başka bir yer imi yerleştirerek bir yer imi ekle.
builder.StartBookmark("Bookmark 1");
builder.Writeln("Text inside Bookmark 1.");

builder.StartBookmark("Bookmark 2");
builder.Writeln("Text inside Bookmark 1 and 2.");
builder.EndBookmark("Bookmark 2");

builder.Writeln("Text inside Bookmark 1.");
builder.EndBookmark("Bookmark 1");

// Başka bir yer imi ekle.
builder.StartBookmark("Bookmark 3");
builder.Writeln("Text inside Bookmark 3.");
builder.EndBookmark("Bookmark 3");

// .pdf'e kaydederken, yer imlerine açılır menü aracılığıyla erişilebilir ve çoğu okuyucu tarafından bağlantı noktası olarak kullanılabilir.
// Yer imleri ayrıca anahat düzeyleri için sayısal değerlere sahip olabilir,
// okuyucuda daraltıldığında daha yüksek seviyeli alt girdileri gizlemek için daha düşük seviyeli ana hat girdilerinin etkinleştirilmesi.
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

// "Yer İşareti 1" için yalnızca anahat düzeyi tanımı kalacak şekilde iki öğeyi kaldırabiliriz.
outlineLevels.RemoveAt(2);
outlineLevels.Remove("Bookmark 2");

// Dokuz anahat seviyesi vardır. Numaralandırmaları kaydetme işlemi sırasında optimize edilecektir.
// Bu durumda "5" ve "9" seviyeleri "2" ve "3" olacaktır.
outlineLevels.Add("Bookmark 2", 5);
outlineLevels.Add("Bookmark 3", 9);

doc.Save(ArtifactsDir + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

// Bu koleksiyonu boşaltmak yer imlerini koruyacak ve hepsini aynı anahat düzeyine yerleştirecektir.
outlineLevels.Clear();
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
