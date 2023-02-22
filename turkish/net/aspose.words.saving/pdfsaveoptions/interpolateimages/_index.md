---
title: PdfSaveOptions.InterpolateImages
second_title: Aspose.Words for .NET API Referansı
description: PdfSaveOptions mülk. Görüntü enterpolasyonunun uygun bir okuyucu tarafından gerçekleştirilip gerçekleştirilmeyeceğini gösteren bir bayrak. Ne zamanyanlış belirtilirse bayrak çıktı belgesine yazılmaz ve bunun yerine okuyucunun varsayılan davranışı kullanılır.
type: docs
weight: 180
url: /tr/net/aspose.words.saving/pdfsaveoptions/interpolateimages/
---
## PdfSaveOptions.InterpolateImages property

Görüntü enterpolasyonunun uygun bir okuyucu tarafından gerçekleştirilip gerçekleştirilmeyeceğini gösteren bir bayrak. Ne zaman`yanlış` belirtilirse, bayrak çıktı belgesine yazılmaz ve bunun yerine okuyucunun varsayılan davranışı kullanılır.

```csharp
public bool InterpolateImages { get; set; }
```

### Notlar

Bir kaynak görüntünün çözünürlüğü çıktı aygıtının çözünürlüğünden önemli ölçüde düşük olduğunda, her kaynak örneği birçok aygıt pikselini kapsar. Sonuç olarak, görüntüler pürüzlü veya bloklu görünebilir. Bu görsel yapaylıklar, oluşturma sırasında bir görüntü enterpolasyon algoritması uygulanarak azaltılabilir. Bir kaynak örneğin kapsadığı tüm pikselleri aynı renkle boyamak yerine, görüntü enterpolasyonu düzgün bir görüntü oluşturmaya çalışır. bitişik örnek değerler arasında geçiş.

Uyumlu bir Okuyucu, PDF'nin bu özelliğini uygulamamayı seçebilir, veya istediği herhangi bir özel enterpolasyon uygulamasını kullanabilir.

Varsayılan değer`yanlış`.

Enterpolasyon bayrağı, PDF/A uyumluluğu tarafından yasaklanmıştır.`yanlış` değer, PDF/A'ya kaydedilirken otomatik olarak kullanılacaktır .

### Örnekler

Bir belgeyi PDF'ye kaydederken görüntüler üzerinde nasıl enterpolasyon yapılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image img = Image.FromFile(ImageDir + "Transparent background logo.png");
builder.InsertImage(img);

// Belgenin "Kaydet" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme şeklini değiştirmek için.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Bu belgeyi açan okuyucunun görüntüleri enterpolasyon yapmasını sağlamak için "InterpolateImages" özelliğini "true" olarak ayarlayın.
// Çözünürlükleri belgeyi görüntüleyen aygıtın çözünürlüğünden daha düşük olmalıdır.
// Okuyucunun herhangi bir enterpolasyon uygulamaması için "InterpolateImages" özelliğini "false" olarak ayarlayın.
saveOptions.InterpolateImages = interpolateImages;

// Bu dökümanı Adobe Acrobat gibi bir okuyucu ile açtığımızda görüntüyü yakınlaştırmamız gerekecek.
// belgeyi etkin olarak kaydettiysek enterpolasyon etkisini görmek için.
doc.Save(ArtifactsDir + "PdfSaveOptions.InterpolateImages.pdf", saveOptions);
```

İşlenen belgelerdeki bir görüntünün kalitesinin nasıl iyileştirileceğini gösterir (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Image image = Image.Decode(ImageDir + "Transparent background logo.png"))
    builder.InsertImage(image);

// Belgenin "Kaydet" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme şeklini değiştirmek için.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Bu belgeyi açan okuyucunun görüntüleri enterpolasyon yapmasını sağlamak için "InterpolateImages" özelliğini "true" olarak ayarlayın.
// Çözünürlükleri belgeyi görüntüleyen aygıtın çözünürlüğünden daha düşük olmalıdır.
// Okuyucunun herhangi bir enterpolasyon uygulamaması için "InterpolateImages" özelliğini "false" olarak ayarlayın.
saveOptions.InterpolateImages = interpolateImages;

// Bu dökümanı Adobe Acrobat gibi bir okuyucu ile açtığımızda görüntüyü yakınlaştırmamız gerekecek.
// belgeyi etkin olarak kaydettiysek enterpolasyon etkisini görmek için.
doc.Save(ArtifactsDir + "PdfSaveOptions.InterpolateImagesNetStandard2.pdf", saveOptions);
```

### Ayrıca bakınız

* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../pdfsaveoptions/)
* toplantı [Aspose.Words](../../../)


