---
title: DocumentBuilder.StartColumnBookmark
linktitle: StartColumnBookmark
articleTitle: StartColumnBookmark
second_title: .NET için Aspose.Words
description: Belge gezintisini ve organizasyonunu geliştirmek için DocumentBuilder'ın StartColumnBookmark yöntemini kullanarak tablo hücresi konumlarını kolayca sütun yer imleri olarak işaretleyin.
type: docs
weight: 660
url: /tr/net/aspose.words/documentbuilder/startcolumnbookmark/
---
## DocumentBuilder.StartColumnBookmark method

Belgedeki geçerli konumu bir sütun yer imi başlangıcı olarak işaretler. Konum bir tablo hücresinde olmalıdır.

```csharp
public BookmarkStart StartColumnBookmark(string bookmarkName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| bookmarkName | String | Yer iminin adı. |

### Geri dönüş değeri

Az önce oluşturulan yer imi başlangıç düğümü.

## Notlar

Bir sütun yer imi, bir satır aralığındaki bir veya daha fazla sütunu kapsar. Geçerli bir yer imi oluşturmak için you her ikisini de çağırmanız gerekir`StartColumnBookmark` Ve[`EndColumnBookmark`](../endcolumnbookmark/) aynı ile*bookmarkName* parametre.

Kötü biçimlendirilmiş yer imleri veya yinelenen adlara sahip yer imleri belge kaydedilirken yok sayılacaktır.

Eklenenin gerçek konumu[`BookmarkStart`](../../bookmarkstart/) düğüm geçerli document oluşturucu konumundan farklı olabilir.

## Örnekler

Sütun yer iminin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

builder.InsertCell();
// 1,2,4,5 numaralı hücreler yer imlerine eklenecek.
builder.StartColumnBookmark("MyBookmark_1");
// Kötü biçimlendirilmiş yer imleri veya yinelenen adlara sahip yer imleri belge kaydedilirken göz ardı edilecektir.
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
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
