---
title: DocumentBuilder.EndBookmark
second_title: Aspose.Words for .NET API Referansı
description: DocumentBuilder yöntem. Belgedeki geçerli konumu yer imi sonu olarak işaretler.
type: docs
weight: 190
url: /tr/net/aspose.words/documentbuilder/endbookmark/
---
## DocumentBuilder.EndBookmark method

Belgedeki geçerli konumu yer imi sonu olarak işaretler.

```csharp
public BookmarkEnd EndBookmark(string bookmarkName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| bookmarkName | String | Yer iminin adı. |

### Geri dönüş değeri

Yeni oluşturulan yer imi bitiş düğümü.

### Notlar

Bir belgedeki yer imleri herhangi bir aralığa yayılabilir ve örtüşebilir. Geçerli bir yer imi oluşturmak için her ikisini de aramanız gerekir[`StartBookmark`](../startbookmark/) ve`EndBookmark` aynısı ile **yer imiAdı** parametresi.

Kötü biçimlendirilmiş yer imleri veya yinelenen adlara sahip yer imleri, belge kaydedildiğinde yok sayılır.

### Örnekler

Bir yer iminin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Geçerli bir yer iminin içinde belge gövde metni olmalıdır
// Eşleşen bir yer imi adıyla oluşturulan BookmarkStart ve BookmarkEnd düğümleri.
builder.StartBookmark("MyBookmark");
builder.Writeln("Hello world!");
builder.EndBookmark("MyBookmark");

Assert.AreEqual(1, doc.Range.Bookmarks.Count);
Assert.AreEqual("MyBookmark", doc.Range.Bookmarks[0].Name);
Assert.AreEqual("Hello world!", doc.Range.Bookmarks[0].Text.Trim());
```

Yerel bir yer işaretine başvuran bir köprünün nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("Bookmark1");
builder.Write("Bookmarked text. ");
builder.EndBookmark("Bookmark1");
builder.Writeln("Text outside of the bookmark.");

// Yer işaretine bağlanan bir KÖPRÜ alanı ekleyin. Alan anahtarlarını geçebiliriz
// başvurulan yer iminin adını içeren bağımsız değişkenin bir parçası olarak "InsertHyperlink" yöntemine.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Link to Bookmark1", @"Bookmark1"" \o ""Hyperlink Tip", true);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

### Ayrıca bakınız

* class [BookmarkEnd](../../bookmarkend/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)


