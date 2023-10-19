---
title: PdfSaveOptions.InterpolateImages
linktitle: InterpolateImages
articleTitle: InterpolateImages
second_title: Aspose.Words for .NET
description: PdfSaveOptions InterpolateImages mülk. Görüntü enterpolasyonunun uyumlu bir okuyucu tarafından gerçekleştirilip gerçekleştirilmeyeceğini belirten bayrak. Ne zamanYANLIŞ belirtildiğinde çıkış belgesine bayrak yazılmaz ve bunun yerine okuyucunun varsayılan davranışı kullanılır C#'da.
type: docs
weight: 210
url: /tr/net/aspose.words.saving/pdfsaveoptions/interpolateimages/
---
## PdfSaveOptions.InterpolateImages property

Görüntü enterpolasyonunun uyumlu bir okuyucu tarafından gerçekleştirilip gerçekleştirilmeyeceğini belirten bayrak. Ne zaman`YANLIŞ` belirtildiğinde, çıkış belgesine bayrak yazılmaz ve bunun yerine okuyucunun varsayılan davranışı kullanılır.

```csharp
public bool InterpolateImages { get; set; }
```

## Notlar

Bir kaynak görüntünün çözünürlüğü çıkış cihazının çözünürlüğünden önemli ölçüde düşük olduğunda, her kaynak örneği birçok cihaz pikselini kapsar. Sonuç olarak, görüntüler pürüzlü veya bloklu görünebilir. Bu görsel yapaylıklar, oluşturma sırasında bir görüntü enterpolasyon algoritması uygulanarak azaltılabilir. Bir kaynak örneğinin kapsadığı tüm pikselleri aynı renkle boyamak yerine, görüntü enterpolasyonu düzgün bir görüntü oluşturmaya çalışır. bitişik örnek değerler arasında geçiş.

Uyumlu bir Okuyucu, PDF'nin bu özelliğini uygulamamayı seçebilir, veya istediği herhangi bir özel enterpolasyon uygulamasını kullanabilir.

Varsayılan değer:`YANLIŞ`.

Enterpolasyon bayrağı PDF/A uyumluluğu nedeniyle yasaklanmıştır.`YANLIŞ` PDF/A'ya kaydederken otomatik olarak değeri kullanılacaktır.

## Örnekler

Bir belgeyi PDF'ye kaydederken görüntüler üzerinde enterpolasyonun nasıl gerçekleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image img = Image.FromFile(ImageDir + "Transparent background logo.png");
builder.InsertImage(img);

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Bu belgeyi açan okuyucunun görselleri enterpolasyona tabi tutmasını sağlamak için "InterpulateImages" özelliğini "true" olarak ayarlayın.
// Çözünürlükleri, belgeyi görüntüleyen cihazın çözünürlüğünden daha düşük olmalıdır.
// Okuyucunun herhangi bir enterpolasyon uygulamamasını sağlamak için "InterpulateImages" özelliğini "false" olarak ayarlayın.
saveOptions.InterpolateImages = interpolateImages;

// Bu belgeyi Adobe Acrobat gibi bir okuyucu ile açtığımızda görseli yakınlaştırmamız gerekecek
// belgeyi etkin olarak kaydettiysek enterpolasyon efektini görmek için.
doc.Save(ArtifactsDir + "PdfSaveOptions.InterpolateImages.pdf", saveOptions);
```

İşlenen belgelerdeki görüntünün kalitesinin nasıl iyileştirileceğini gösterir (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Image image = Image.Decode(ImageDir + "Transparent background logo.png"))
    builder.InsertImage(image);

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Bu belgeyi açan okuyucunun görselleri enterpolasyona tabi tutmasını sağlamak için "InterpulateImages" özelliğini "true" olarak ayarlayın.
// Çözünürlükleri, belgeyi görüntüleyen cihazın çözünürlüğünden daha düşük olmalıdır.
// Okuyucunun herhangi bir enterpolasyon uygulamamasını sağlamak için "InterpulateImages" özelliğini "false" olarak ayarlayın.
saveOptions.InterpolateImages = interpolateImages;

// Bu belgeyi Adobe Acrobat gibi bir okuyucu ile açtığımızda görseli yakınlaştırmamız gerekecek
// belgeyi etkin olarak kaydettiysek enterpolasyon efektini görmek için.
doc.Save(ArtifactsDir + "PdfSaveOptions.InterpolateImagesNetStandard2.pdf", saveOptions);
```

### Ayrıca bakınız

* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
