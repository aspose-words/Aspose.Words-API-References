---
title: BookmarksOutlineLevelCollection.Add
second_title: Aspose.Words for .NET API Referansı
description: BookmarksOutlineLevelCollection yöntem. Koleksiyona bir yer işareti ekler.
type: docs
weight: 40
url: /tr/net/aspose.words.saving/bookmarksoutlinelevelcollection/add/
---
## BookmarksOutlineLevelCollection.Add method

Koleksiyona bir yer işareti ekler.

```csharp
public void Add(string name, int outlineLevel)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| name | String | Eklenecek yer işaretinin büyük/küçük harfe duyarlı olmayan adı. |
| outlineLevel | Int32 | Yer iminin anahat düzeyi. Geçerli aralık 0 ila 9'dur. |

### Örnekler

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

* class [BookmarksOutlineLevelCollection](../)
* ad alanı [Aspose.Words.Saving](../../bookmarksoutlinelevelcollection/)
* toplantı [Aspose.Words](../../../)


