---
title: OutlineOptions.BookmarksOutlineLevels
linktitle: BookmarksOutlineLevels
articleTitle: BookmarksOutlineLevels
second_title: .NET için Aspose.Words
description: Gelişmiş gezinme ve kullanıcı deneyimi için yer imlerinizin hiyerarşisini özelleştirmek üzere OutlineOptions'daki BookmarksOutlineLevels özelliğini keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words.saving/outlineoptions/bookmarksoutlinelevels/
---
## OutlineOptions.BookmarksOutlineLevels property

Bireysel yer imlerinin anahat düzeyini belirtmeye izin verir.

```csharp
public BookmarksOutlineLevelCollection BookmarksOutlineLevels { get; }
```

## Notlar

Bu koleksiyonda yer imi düzeyi belirtilmemişse o zaman[`DefaultBookmarksOutlineLevel`](../defaultbookmarksoutlinelevel/) değer kullanılır.

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

* class [BookmarksOutlineLevelCollection](../../bookmarksoutlinelevelcollection/)
* class [OutlineOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
