---
title: BuiltInDocumentProperties.Thumbnail
linktitle: Thumbnail
articleTitle: Thumbnail
second_title: .NET için Aspose.Words
description: BuiltInDocumentProperties ile belgenizin görsel çekiciliğini yönetin. Gelişmiş sunum ve organizasyon için küçük resim görüntülerini kolayca alın veya ayarlayın.
type: docs
weight: 310
url: /tr/net/aspose.words.properties/builtindocumentproperties/thumbnail/
---
## BuiltInDocumentProperties.Thumbnail property

Belgenin küçük resmini alır veya ayarlar.

```csharp
public byte[] Thumbnail { get; set; }
```

### istisnalar

| istisna | şart |
| --- | --- |
| InvalidOperationException | Görüntü geçersizse veya biçimi belirli bir belge biçimi için desteklenmiyorsa atılır. |

## Notlar

Şimdilik bu özellik yalnızca bir belge ePub'a aktarılırken kullanılıyor, diğer belge biçimlerinden okunmuyor veya bu biçimlere yazılamıyor.

Bu özelliğe, herhangi bir formattaki görüntü ayarlanabilir, ancak format, dışa aktarma sırasında kontrol edilir.

ePub yayınında yalnızca gif, jpeg ve png formatındaki resimler kullanılabilir.

## Örnekler

Epub olarak kaydettiğimiz bir belgeye küçük resim eklemenin nasıl yapılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// "Küçük Resim" özelliği eklediğimiz resim verilerini içeren bir belgeyi Epub olarak kaydedersek,
// Bu belgeyi açan bir okuyucu, ilk sayfadan önce resmi görüntüleyebilir.
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

byte[] thumbnailBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");
properties.Thumbnail = thumbnailBytes;

doc.Save(ArtifactsDir + "DocumentProperties.Thumbnail.epub");

// Bir belgenin küçük resmini çıkarıp yerel dosya sistemine kaydedebiliriz.
DocumentProperty thumbnail = doc.BuiltInDocumentProperties["Thumbnail"];
File.WriteAllBytes(ArtifactsDir + "DocumentProperties.Thumbnail.gif", thumbnail.ToByteArray());
```

### Ayrıca bakınız

* class [BuiltInDocumentProperties](../)
* ad alanı [Aspose.Words.Properties](../../../aspose.words.properties/)
* toplantı [Aspose.Words](../../../)
