---
title: PdfSaveOptions.JpegQuality
linktitle: JpegQuality
articleTitle: JpegQuality
second_title: .NET için Aspose.Words
description: PDF resimlerinizi PdfSaveOptions'ın JpegQuality özelliğiyle optimize edin; böylece çarpıcı belge görselleri için JPEG kalitesini kontrol edebilirsiniz.
type: docs
weight: 220
url: /tr/net/aspose.words.saving/pdfsaveoptions/jpegquality/
---
## PdfSaveOptions.JpegQuality property

PDF belgesinin içindeki JPEG görüntülerinin kalitesini belirleyen bir değeri alır veya ayarlar.

```csharp
public int JpegQuality { get; set; }
```

## Notlar

Varsayılan değer 100'dür.

Bu özellik, aşağıdakilerle birlikte kullanılır:[`ImageCompression`](../imagecompression/) seçenek.

Yalnızca belge JPEG görüntüleri içerdiğinde etkilidir.

PDF formatında kaydederken bir belgenin içindeki resimlerin kalitesini almak veya ayarlamak için bu özelliği kullanın. Değer 0 ile 100 arasında değişebilir; burada 0 en kötü kalite ancak maksimum sıkıştırma, 100 ise en iyi kalite ancak minimum sıkıştırma anlamına gelir. Kalite 100 ve kaynak resim JPEG ise, sıkıştırma yok demektir - orijinal baytlar kaydedilecektir.

## Örnekler

PDF'ye dönüştürdüğümüz bir belgedeki tüm resimler için bir sıkıştırma türünün nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jpeg image:");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertParagraph();
builder.Writeln("Png image:");
builder.InsertImage(ImageDir + "Transparent background logo.png");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
// "ImageCompression" özelliğini "PdfImageCompression.Auto" olarak ayarlayın
// Çıktı PDF'inde yer alan Jpeg görüntülerinin kalitesini kontrol etmek için "ImageCompression" özelliği.
// "ImageCompression" özelliğini "PdfImageCompression.Jpeg" olarak ayarlayın
// Çıktı PDF'inde yer alan tüm görsellerin kalitesini kontrol etmek için "ImageCompression" özelliği.
pdfSaveOptions.ImageCompression = pdfImageCompression;
// Görüntü kalitesinden ödün vererek sıkıştırmayı artırmak için "JpegQuality" özelliğini "10" olarak ayarlayın.
pdfSaveOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "PdfSaveOptions.ImageCompression.pdf", pdfSaveOptions);
```

### Ayrıca bakınız

* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
