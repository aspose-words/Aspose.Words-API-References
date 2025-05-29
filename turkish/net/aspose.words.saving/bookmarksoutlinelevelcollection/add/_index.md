---
title: BookmarksOutlineLevelCollection.Add
linktitle: Add
articleTitle: Add
second_title: .NET için Aspose.Words
description: BookmarksOutlineLevelCollection Ekleme yöntemiyle projenizi nasıl geliştirebileceğinizi keşfedin; daha iyi bir organizasyon için koleksiyonunuza yer imlerini zahmetsizce ekleyin.
type: docs
weight: 40
url: /tr/net/aspose.words.saving/bookmarksoutlinelevelcollection/add/
---
## BookmarksOutlineLevelCollection.Add method

Koleksiyona bir yer imi ekler.

```csharp
public void Add(string name, int outlineLevel)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| name | String | Eklenecek yer iminin büyük/küçük harfe duyarlı olmayan adı. |
| outlineLevel | Int32 | Yer iminin anahat seviyesi. Geçerli aralık 0 ila 9'dur. |

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

* class [BookmarksOutlineLevelCollection](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
