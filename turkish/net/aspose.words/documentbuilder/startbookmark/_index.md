---
title: DocumentBuilder.StartBookmark
linktitle: StartBookmark
articleTitle: StartBookmark
second_title: Aspose.Words for .NET
description: DocumentBuilder StartBookmark yöntem. Belgedeki geçerli konumu yer imi başlangıcı olarak işaretler C#'da.
type: docs
weight: 610
url: /tr/net/aspose.words/documentbuilder/startbookmark/
---
## DocumentBuilder.StartBookmark method

Belgedeki geçerli konumu yer imi başlangıcı olarak işaretler.

```csharp
public BookmarkStart StartBookmark(string bookmarkName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| bookmarkName | String | Yer iminin adı. |

### Geri dönüş değeri

Yeni oluşturulan yer imi başlangıç düğümü.

## Notlar

Bir belgedeki yer imleri herhangi bir aralıkla örtüşebilir ve yayılabilir. Geçerli bir yer imi oluşturmak için her ikisini de aramanız gerekir`StartBookmark` Ve[`EndBookmark`](../endbookmark/) aynısıyla*bookmarkName* parametresi.

Kötü biçimlendirilmiş yer imleri veya yinelenen adlara sahip yer imleri, belge kaydedildiğinde göz ardı edilecektir.

## Örnekler

Yer iminin nasıl oluşturulduğunu gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Geçerli bir yer iminin, belge gövde metnini içine alması gerekir
// Eşleşen bir yer imi adıyla oluşturulan BookmarkStart ve BookmarkEnd düğümleri.
builder.StartBookmark("MyBookmark");
builder.Writeln("Hello world!");
builder.EndBookmark("MyBookmark");

Assert.AreEqual(1, doc.Range.Bookmarks.Count);
Assert.AreEqual("MyBookmark", doc.Range.Bookmarks[0].Name);
Assert.AreEqual("Hello world!", doc.Range.Bookmarks[0].Text.Trim());
```

Yerel bir yer imine başvuran bir köprünün nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("Bookmark1");
builder.Write("Bookmarked text. ");
builder.EndBookmark("Bookmark1");
builder.Writeln("Text outside of the bookmark.");

// Yer imine bağlanan bir KÖPRÜ alanı ekleyin. Alan anahtarlarını geçebiliriz
// başvurulan yer iminin adını içeren bağımsız değişkenin bir parçası olarak "InsertHyperlink" yöntemine.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Link to Bookmark1", @"Bookmark1"" \o ""Hyperlink Tip", true);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

### Ayrıca bakınız

* class [BookmarkStart](../../bookmarkstart/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
