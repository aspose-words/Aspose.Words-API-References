---
title: DocumentBuilder.EndColumnBookmark
linktitle: EndColumnBookmark
articleTitle: EndColumnBookmark
second_title: .NET için Aspose.Words
description: Belgenizdeki bir sütunun sonunu kolayca işaretlemek için DocumentBuilder'ın EndColumnBookmark yöntemini kullanın. Tablo yönetimini hassasiyetle geliştirin!
type: docs
weight: 220
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

Az önce oluşturulan yer imi bitiş düğümü.

## Notlar

Bir sütun yer imi, bir satır aralığındaki bir veya daha fazla sütunu kapsar. Geçerli bir yer imi oluşturmak için you her ikisini de çağırmanız gerekir[`StartColumnBookmark`](../startcolumnbookmark/) Ve`EndColumnBookmark` aynı ile*bookmarkName* parametre.

Kötü biçimlendirilmiş yer imleri veya yinelenen adlara sahip yer imleri belge kaydedilirken yok sayılacaktır.

Eklenenin gerçek konumu[`BookmarkEnd`](../../bookmarkend/) düğüm geçerli document oluşturucu konumundan farklı olabilir.

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

* class [BookmarkEnd](../../bookmarkend/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
