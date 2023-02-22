---
title: BookmarksOutlineLevelCollection.Item
second_title: Aspose.Words for .NET API Referansı
description: BookmarksOutlineLevelCollection mülk. Yer imi adına göre bir yer imi anahat düzeyi alır veya ayarlar.
type: docs
weight: 30
url: /tr/net/aspose.words.saving/bookmarksoutlinelevelcollection/item/
---
## BookmarksOutlineLevelCollection indexer (1 of 2)

Yer imi adına göre bir yer imi anahat düzeyi alır veya ayarlar.

```csharp
public int this[string name] { get; set; }
```

| Parametre | Tanım |
| --- | --- |
| name | Yer işaretinin büyük/küçük harfe duyarsız adı. |

### Geri dönüş değeri

Yer işaretinin anahat düzeyi. Geçerli aralık 0 ila 9'dur.

### Örnekler

Yer imleri için anahat düzeylerinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// İçinde başka bir yer imi bulunan bir yer imi ekleyin.
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

// .pdf dosyasına kaydederken, yer imlerine bir açılır menü aracılığıyla erişilebilir ve çoğu okuyucu tarafından sabitleyici olarak kullanılabilir.
// Yer imleri, anahat seviyeleri için sayısal değerlere de sahip olabilir,
// okuyucuda daraltıldığında daha yüksek seviyeli alt girişleri gizlemek için alt seviye anahat girişlerini etkinleştirme.
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

// "Yer İşareti 1" için yalnızca anahat düzeyi ataması kalacak şekilde iki öğeyi kaldırabiliriz.
outlineLevels.RemoveAt(2);
outlineLevels.Remove("Bookmark 2");

// Dokuz anahat seviyesi vardır. Numaralandırma, kaydetme işlemi sırasında optimize edilecektir.
// Bu durumda "5" ve "9" seviyeleri "2" ve "3" olacaktır.
outlineLevels.Add("Bookmark 2", 5);
outlineLevels.Add("Bookmark 3", 9);

doc.Save(ArtifactsDir + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

// Bu koleksiyonun boşaltılması, yer imlerini koruyacak ve hepsini aynı anahat düzeyine yerleştirecektir.
outlineLevels.Clear();
```

### Ayrıca bakınız

* class [BookmarksOutlineLevelCollection](../)
* ad alanı [Aspose.Words.Saving](../../bookmarksoutlinelevelcollection/)
* toplantı [Aspose.Words](../../../)

---

## BookmarksOutlineLevelCollection indexer (2 of 2)

Belirtilen dizinde bir yer imi anahat düzeyi alır veya ayarlar.

```csharp
public int this[int index] { get; set; }
```

| Parametre | Tanım |
| --- | --- |
| index | Yer iminin sıfır tabanlı dizini. |

### Geri dönüş değeri

Yer işaretinin anahat düzeyi. Geçerli aralık 0 ila 9'dur.

### Örnekler

Yer imleri için anahat düzeylerinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// İçinde başka bir yer imi bulunan bir yer imi ekleyin.
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

// .pdf dosyasına kaydederken, yer imlerine bir açılır menü aracılığıyla erişilebilir ve çoğu okuyucu tarafından sabitleyici olarak kullanılabilir.
// Yer imleri, anahat seviyeleri için sayısal değerlere de sahip olabilir,
// okuyucuda daraltıldığında daha yüksek seviyeli alt girişleri gizlemek için alt seviye anahat girişlerini etkinleştirme.
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

// "Yer İşareti 1" için yalnızca anahat düzeyi ataması kalacak şekilde iki öğeyi kaldırabiliriz.
outlineLevels.RemoveAt(2);
outlineLevels.Remove("Bookmark 2");

// Dokuz anahat seviyesi vardır. Numaralandırma, kaydetme işlemi sırasında optimize edilecektir.
// Bu durumda "5" ve "9" seviyeleri "2" ve "3" olacaktır.
outlineLevels.Add("Bookmark 2", 5);
outlineLevels.Add("Bookmark 3", 9);

doc.Save(ArtifactsDir + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

// Bu koleksiyonun boşaltılması, yer imlerini koruyacak ve hepsini aynı anahat düzeyine yerleştirecektir.
outlineLevels.Clear();
```

### Ayrıca bakınız

* class [BookmarksOutlineLevelCollection](../)
* ad alanı [Aspose.Words.Saving](../../bookmarksoutlinelevelcollection/)
* toplantı [Aspose.Words](../../../)


