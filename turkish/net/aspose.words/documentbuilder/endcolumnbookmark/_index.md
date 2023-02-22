---
title: DocumentBuilder.EndColumnBookmark
second_title: Aspose.Words for .NET API Referansı
description: DocumentBuilder yöntem. Belgedeki geçerli konumu bir sütun yer imi sonu olarak işaretler. Konum bir tablo hücresinde olmalıdır.
type: docs
weight: 200
url: /tr/net/aspose.words/documentbuilder/endcolumnbookmark/
---
## DocumentBuilder.EndColumnBookmark method

Belgedeki geçerli konumu bir sütun yer imi sonu olarak işaretler. Konum bir tablo hücresinde olmalıdır.

```csharp
public BookmarkEnd EndColumnBookmark(string bookmarkName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| bookmarkName | String | Yer iminin adı. |

### Geri dönüş değeri

Yeni oluşturulan yer imi bitiş düğümü.

### Notlar

Bir sütun yer imi, bir dizi satırdaki bir veya daha fazla sütunu kapsar. Geçerli bir yer imi oluşturmak için you her ikisini de aramanız gerekir[`StartColumnBookmark`](../startcolumnbookmark/) ve`EndColumnBookmark` same ile **yer imiAdı** parametre.

Kötü biçimlendirilmiş yer imleri veya yinelenen adlara sahip yer imleri, belge kaydedildiğinde yok sayılır.

Eklenen öğenin gerçek konumu[`BookmarkEnd`](../../bookmarkend/) düğüm, geçerli document oluşturucu konumundan farklı olabilir.

### Örnekler

Sütun yer iminin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

builder.InsertCell();
// 1,2,4,5 hücreleri işaretlenecek.
builder.StartColumnBookmark("MyBookmark_1");
// Kötü biçimli yer imleri veya yinelenen adlara sahip yer imleri, belge kaydedildiğinde yok sayılır.
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

* class [BookmarkEnd](../../bookmarkend/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)


