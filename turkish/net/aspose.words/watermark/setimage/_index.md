---
title: Watermark.SetImage
linktitle: SetImage
articleTitle: SetImage
second_title: .NET için Aspose.Words
description: Belgelerinizi Watermark SetImage yöntemiyle geliştirin. Profesyonel bir dokunuş için çarpıcı resim filigranlarını zahmetsizce ekleyin.
type: docs
weight: 30
url: /tr/net/aspose.words/watermark/setimage/
---
## SetImage(*Image*) {#setimage}

Belgeye Resim filigranı ekler.

```csharp
public void SetImage(Image image)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| image | Image | Filigran olarak görüntülenen resim. |

### istisnalar

| istisna | şart |
| --- | --- |
| ArgumentNullException | Görüntü olduğunda atılır`hükümsüz` . |

## Örnekler

Yerel dosya sistemindeki bir görüntüden filigranın nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

            // Resim filigranının görünümünü ImageWatermarkOptions nesnesiyle değiştirin,
            // daha sonra bir resim dosyasından filigran oluştururken bunu geçirin.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET461_OR_GREATER || JAVA
            // Resim eklemek için farklı seçeneklerimiz var:
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);

            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"));

            doc.Watermark.SetImage(ImageDir + "Logo.jpg", imageWatermarkOptions);
#elif NET5_0_OR_GREATER
            using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
            {
                doc.Watermark.SetImage(image, imageWatermarkOptions);
            }
#endif

            doc.Save(ArtifactsDir + "Document.ImageWatermark.docx");
```

### Ayrıca bakınız

* class [Watermark](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## SetImage(*Image, [ImageWatermarkOptions](../../imagewatermarkoptions/)*) {#setimage_1}

Belgeye Resim filigranı ekler.

```csharp
public void SetImage(Image image, ImageWatermarkOptions options)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| image | Image | Filigran olarak görüntülenen resim. |
| options | ImageWatermarkOptions | Resim filigranı için ek seçenekleri tanımlar. |

### istisnalar

| istisna | şart |
| --- | --- |
| ArgumentNullException | Görüntü olduğunda atılır`hükümsüz` . |

## Notlar

Eğer[`ImageWatermarkOptions`](../../imagewatermarkoptions/) dır`hükümsüz`, filigran varsayılan seçeneklerle ayarlanacaktır.

## Örnekler

Yerel dosya sistemindeki bir görüntüden filigranın nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

            // Resim filigranının görünümünü ImageWatermarkOptions nesnesiyle değiştirin,
            // daha sonra bir resim dosyasından filigran oluştururken bunu geçirin.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET461_OR_GREATER || JAVA
            // Resim eklemek için farklı seçeneklerimiz var:
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);

            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"));

            doc.Watermark.SetImage(ImageDir + "Logo.jpg", imageWatermarkOptions);
#elif NET5_0_OR_GREATER
            using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
            {
                doc.Watermark.SetImage(image, imageWatermarkOptions);
            }
#endif

            doc.Save(ArtifactsDir + "Document.ImageWatermark.docx");
```

### Ayrıca bakınız

* class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* class [Watermark](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## SetImage(*string, [ImageWatermarkOptions](../../imagewatermarkoptions/)*) {#setimage_3}

Belgeye Resim filigranı ekler.

```csharp
public void SetImage(string imagePath, ImageWatermarkOptions options)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| imagePath | String | Filigran olarak görüntülenen resim dosyasının yolu. |
| options | ImageWatermarkOptions | Resim filigranı için ek seçenekleri tanımlar. |

### istisnalar

| istisna | şart |
| --- | --- |
| ArgumentNullException | Yol olduğunda fırlatır`hükümsüz` . |

## Notlar

Eğer[`ImageWatermarkOptions`](../../imagewatermarkoptions/) dır`hükümsüz`, filigran varsayılan seçeneklerle ayarlanacaktır.

## Örnekler

Yerel dosya sistemindeki bir görüntüden filigranın nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

            // Resim filigranının görünümünü ImageWatermarkOptions nesnesiyle değiştirin,
            // daha sonra bir resim dosyasından filigran oluştururken bunu geçirin.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET461_OR_GREATER || JAVA
            // Resim eklemek için farklı seçeneklerimiz var:
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);

            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"));

            doc.Watermark.SetImage(ImageDir + "Logo.jpg", imageWatermarkOptions);
#elif NET5_0_OR_GREATER
            using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
            {
                doc.Watermark.SetImage(image, imageWatermarkOptions);
            }
#endif

            doc.Save(ArtifactsDir + "Document.ImageWatermark.docx");
```

### Ayrıca bakınız

* class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* class [Watermark](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## SetImage(*Stream, [ImageWatermarkOptions](../../imagewatermarkoptions/)*) {#setimage_2}

Belgeye Resim filigranı ekler.

```csharp
public void SetImage(Stream imageStream, ImageWatermarkOptions options)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| imageStream | Stream | Filigran olarak görüntülenen resim verilerini içeren akış. |
| options | ImageWatermarkOptions | Resim filigranı için ek seçenekleri tanımlar. |

### istisnalar

| istisna | şart |
| --- | --- |
| ArgumentNullException | Yol olduğunda fırlatır`hükümsüz` . |

## Notlar

Eğer[`ImageWatermarkOptions`](../../imagewatermarkoptions/) dır`hükümsüz`, filigran varsayılan seçeneklerle ayarlanacaktır.

## Örnekler

Bir resim akışından filigranın nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

// Resim filigranının görünümünü ImageWatermarkOptions nesnesiyle değiştirin,
// daha sonra bir resim dosyasından filigran oluştururken bunu geçirin.
ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
imageWatermarkOptions.Scale = 5;

using (FileStream imageStream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open, FileAccess.Read))
    doc.Watermark.SetImage(imageStream, imageWatermarkOptions);

doc.Save(ArtifactsDir + "Document.ImageWatermarkStream.docx");
```

### Ayrıca bakınız

* class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* class [Watermark](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
