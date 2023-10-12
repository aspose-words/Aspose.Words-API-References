---
title: DocumentBuilder.StartColumnBookmark
second_title: Aspose.Words for .NET API Referansı
description: DocumentBuilder yöntem. Belgedeki geçerli konumu sütun yer işareti başlangıcı olarak işaretler. Konum bir tablo hücresinde olmalıdır.
type: docs
weight: 630
url: /tr/net/aspose.words/documentbuilder/startcolumnbookmark/
---
## DocumentBuilder.StartColumnBookmark method

Belgedeki geçerli konumu sütun yer işareti başlangıcı olarak işaretler. Konum bir tablo hücresinde olmalıdır.

```csharp
public BookmarkStart StartColumnBookmark(string bookmarkName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| bookmarkName | String | Yer iminin adı. |

### Geri dönüş değeri

Yeni oluşturulan yer imi başlangıç düğümü.

### Notlar

Sütun yer işareti, bir satır aralığındaki bir veya daha fazla sütunu kapsar. Geçerli bir yer imi oluşturmak için you her ikisini de aramanız gerekir`StartColumnBookmark` Ve[`EndColumnBookmark`](../endcolumnbookmark/) aynı ile*bookmarkName*parametre.

Kötü biçimlendirilmiş yer imleri veya yinelenen adlara sahip yer imleri, belge kaydedildiğinde göz ardı edilecektir.

Takılan öğenin gerçek konumu[`BookmarkStart`](../../bookmarkstart/) düğümü geçerli document oluşturucu konumundan farklı olabilir.

### Örnekler

Sütun yer işaretinin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

builder.InsertCell();
// 1,2,4,5 numaralı hücreler işaretlenecektir.
builder.StartColumnBookmark("MyBookmark_1");
// Kötü biçimlendirilmiş yer imleri veya yinelenen adlara sahip yer imleri, belge kaydedildiğinde dikkate alınmayacaktır.
builder.StartColumnBookmark("MyBookmark_1");
builder.StartColumnBookmark("BadStartBookmark");
builder.Write("Cell 1");

builder.InsertCell();
builder.Write("Cell 2");

builder.InsertCell();
builder.Write("Cell 3");

builder.EndRow();

builder.InsertCell();
builder.Write("Cell 4");

builder.InsertCell();
builder.Write("Cell 5");
builder.EndColumnBookmark("MyBookmark_1");
builder.EndColumnBookmark("MyBookmark_1");

builder.InsertCell();
builder.Write("Cell 6");

builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "Bookmarks.CreateColumnBookmark.docx");
```

### Ayrıca bakınız

* class [BookmarkStart](../../bookmarkstart/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)


