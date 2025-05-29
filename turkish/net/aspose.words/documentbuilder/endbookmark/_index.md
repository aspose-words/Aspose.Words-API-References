---
title: DocumentBuilder.EndBookmark
linktitle: EndBookmark
articleTitle: EndBookmark
second_title: .NET için Aspose.Words
description: Belgenizdeki bir yer iminin sonunu DocumentBuilder'ın EndBookmark yöntemiyle zahmetsizce işaretleyin, belgenizin organizasyonunu ve gezinmesini geliştirin.
type: docs
weight: 210
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

Az önce oluşturulan yer imi bitiş düğümü.

## Notlar

Bir belgedeki yer imleri herhangi bir aralığı kaplayabilir ve örtüşebilir. Geçerli bir yer imi oluşturmak için her ikisini de çağırmanız gerekir [`StartBookmark`](../startbookmark/) Ve`EndBookmark` aynı şekilde*bookmarkName* parametresi.

Kötü biçimlendirilmiş yer imleri veya yinelenen adlara sahip yer imleri belge kaydedilirken yok sayılacaktır.

## Örnekler

Bir yer imi oluşturmanın nasıl yapıldığını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Geçerli bir yer iminin, belge gövde metninin içine alınması gerekir
// Eşleşen bir yer imi adıyla oluşturulan BookmarkStart ve BookmarkEnd düğümleri.
builder.StartBookmark("MyBookmark");
builder.Writeln("Hello world!");
builder.EndBookmark("MyBookmark");

Assert.AreEqual(1, doc.Range.Bookmarks.Count);
Assert.AreEqual("MyBookmark", doc.Range.Bookmarks[0].Name);
Assert.AreEqual("Hello world!", doc.Range.Bookmarks[0].Text.Trim());
```

Yerel bir yer imine referans veren bir köprü metninin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("Bookmark1");
builder.Write("Bookmarked text. ");
builder.EndBookmark("Bookmark1");
builder.Writeln("Text outside of the bookmark.");

// Yer imine bağlanan bir HYPERLINK alanı ekleyin. Alan anahtarlarını geçebiliriz
// başvurulan yer iminin adını içeren argümanın bir parçası olarak "InsertHyperlink" yöntemine.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
FieldHyperlink hyperlink = (FieldHyperlink)builder.InsertHyperlink("Link to Bookmark1", "Bookmark1", true);
hyperlink.ScreenTip = "Hyperlink Tip";

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

### Ayrıca bakınız

* class [BookmarkEnd](../../bookmarkend/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
