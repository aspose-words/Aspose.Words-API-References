---
title: Document.UpdateThumbnail
second_title: Aspose.Words for .NET API Referansı
description: Document yöntem. GüncellemelerThumbnail belirtilen seçeneklere göre belgenin.
type: docs
weight: 800
url: /tr/net/aspose.words/document/updatethumbnail/
---
## UpdateThumbnail(ThumbnailGeneratingOptions) {#updatethumbnail_1}

Güncellemeler[`Thumbnail`](../../../aspose.words.properties/builtindocumentproperties/thumbnail/) belirtilen seçeneklere göre belgenin.

```csharp
public void UpdateThumbnail(ThumbnailGeneratingOptions options)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| options | ThumbnailGeneratingOptions | Kullanılacak oluşturma seçenekleri. |

### Notlar

[`ThumbnailGeneratingOptions`](../../../aspose.words.rendering/thumbnailgeneratingoptions/) küçük resmin kaynağını, boyutunu ve diğer seçenekleri belirtmenize olanak tanır. Küçük resim oluşturma girişimi başarısız olursa, birini değiştirmez.

### Örnekler

Bir belgenin küçük resminin nasıl güncelleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Bir belgeyi .epub'a kaydederken küçük resim görüntüsünü ayarlamanın iki yolu vardır.
// 1 - Belgenin ilk sayfasını kullanın:
doc.UpdateThumbnail();
doc.Save(ArtifactsDir + "Document.UpdateThumbnail.FirstPage.epub");

// 2 - Belgede bulunan ilk resmi kullanın:
ThumbnailGeneratingOptions options = new ThumbnailGeneratingOptions();
options.ThumbnailSize = new Size(400, 400);
options.GenerateFromFirstPage = false;

doc.UpdateThumbnail(options);
doc.Save(ArtifactsDir + "Document.UpdateThumbnail.FirstImage.epub");
```

### Ayrıca bakınız

* class [ThumbnailGeneratingOptions](../../../aspose.words.rendering/thumbnailgeneratingoptions/)
* class [Document](../)
* ad alanı [Aspose.Words](../../document/)
* toplantı [Aspose.Words](../../../)

---

## UpdateThumbnail() {#updatethumbnail}

Güncellemeler[`Thumbnail`](../../../aspose.words.properties/builtindocumentproperties/thumbnail/) varsayılan seçenekleri kullanarak belgenin.

```csharp
public void UpdateThumbnail()
```

### Örnekler

Bir belgenin küçük resminin nasıl güncelleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Bir belgeyi .epub'a kaydederken küçük resim görüntüsünü ayarlamanın iki yolu vardır.
// 1 - Belgenin ilk sayfasını kullanın:
doc.UpdateThumbnail();
doc.Save(ArtifactsDir + "Document.UpdateThumbnail.FirstPage.epub");

// 2 - Belgede bulunan ilk resmi kullanın:
ThumbnailGeneratingOptions options = new ThumbnailGeneratingOptions();
options.ThumbnailSize = new Size(400, 400);
options.GenerateFromFirstPage = false;

doc.UpdateThumbnail(options);
doc.Save(ArtifactsDir + "Document.UpdateThumbnail.FirstImage.epub");
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../document/)
* toplantı [Aspose.Words](../../../)


