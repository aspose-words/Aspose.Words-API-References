---
title: PdfSaveOptions.JpegQuality
second_title: Aspose.Words for .NET API Referansı
description: PdfSaveOptions mülk. PDF belgesi içindeki JPEG görüntülerinin kalitesini belirleyen bir değer alır veya ayarlar.
type: docs
weight: 220
url: /tr/net/aspose.words.saving/pdfsaveoptions/jpegquality/
---
## PdfSaveOptions.JpegQuality property

PDF belgesi içindeki JPEG görüntülerinin kalitesini belirleyen bir değer alır veya ayarlar.

```csharp
public int JpegQuality { get; set; }
```

### Notlar

Varsayılan değer 100'dür.

Bu özellik aşağıdakilerle birlikte kullanılır:[`ImageCompression`](../imagecompression/) seçenek.

Yalnızca bir belge JPEG görüntüleri içerdiğinde etkili olur.

PDF formatında kaydederken belge içindeki görüntülerin kalitesini almak veya ayarlamak için bu özelliği kullanın. Değer 0 ila 100 arasında değişebilir; burada 0 en kötü kalite ancak maksimum sıkıştırma anlamına gelir ve 100 en iyi kalite ancak minimum sıkıştırma anlamına gelir. Kalite ise 100'dür ve kaynak görüntü JPEG'dir, bu sıkıştırma olmadığı anlamına gelir - orijinal baytlar kaydedilecektir.

### Örnekler

PDF'ye dönüştürdüğümüz bir belgedeki tüm görüntüler için sıkıştırma türünün nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jpeg image:");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertParagraph();
builder.Writeln("Png image:");
builder.InsertImage(ImageDir + "Transparent background logo.png");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

// "ImageCompression" özelliğini kullanmak için "PdfImageCompression.Auto" olarak ayarlayın.
// Çıktı PDF'sinde yer alan Jpeg görüntülerinin kalitesini kontrol etmek için "ImageCompression" özelliği.
// "ImageCompression" özelliğini kullanmak için "PdfImageCompression.Jpeg" olarak ayarlayın.
// Çıktı PDF'sinde yer alan tüm görüntülerin kalitesini kontrol etmek için "ImageCompression" özelliği.
pdfSaveOptions.ImageCompression = pdfImageCompression;

// Görüntü kalitesinden ödün vererek sıkıştırmayı güçlendirmek için "JpegQuality" özelliğini "10" olarak ayarlayın.
pdfSaveOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "PdfSaveOptions.ImageCompression.pdf", pdfSaveOptions);
```

### Ayrıca bakınız

* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../pdfsaveoptions/)
* toplantı [Aspose.Words](../../../)


