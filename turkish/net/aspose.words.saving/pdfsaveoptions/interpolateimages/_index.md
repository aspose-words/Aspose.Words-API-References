---
title: PdfSaveOptions.InterpolateImages
linktitle: InterpolateImages
articleTitle: InterpolateImages
second_title: .NET için Aspose.Words
description: Belgelerinizdeki görüntü kalitesini artıran önemli bir özellik olan PdfSaveOptions' InterpolateImages özelliğini keşfedin. PDF'lerinizi zahmetsizce optimize edin!
type: docs
weight: 210
url: /tr/net/aspose.words.saving/pdfsaveoptions/interpolateimages/
---
## PdfSaveOptions.InterpolateImages property

Görüntü enterpolasyonunun uygun bir okuyucu tarafından yapılıp yapılmayacağını belirten bir bayrak. Ne zaman`YANLIŞ` belirtildiğinde, bayrak çıktı belgesine yazılmaz ve bunun yerine okuyucunun varsayılan davranışı kullanılır.

```csharp
public bool InterpolateImages { get; set; }
```

## Notlar

Bir kaynak görüntünün çözünürlüğü çıktı aygıtının çözünürlüğünden önemli ölçüde düşük olduğunda, her kaynak örneği birçok aygıt pikselini kapsar. Sonuç olarak, görüntüler engebeli veya bloklu görünebilir. Bu görsel eserler, işleme sırasında bir görüntü enterpolasyon algoritması uygulanarak azaltılabilir. Bir kaynak örneğinin kapsadığı tüm pikselleri aynı renkle boyamak yerine, görüntü enterpolasyonu bitişik örnek değerleri arasında yumuşak bir geçiş üretmeye çalışır.

Uyumlu bir Okuyucu, PDF'nin bu özelliğini uygulamamayı seçebilir, veya istediği herhangi bir özel enterpolasyon uygulamasını kullanabilir.

Varsayılan değer:`YANLIŞ`.

PDF/A uyumluluğu gereği enterpolasyon bayrağı yasaktır.`YANLIŞ` PDF/A'ya kaydederken değer otomatik olarak kullanılacaktır .

## Örnekler

Bir belgeyi PDF'e kaydederken görüntüler üzerinde enterpolasyonun nasıl gerçekleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Transparent background logo.png");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
PdfSaveOptions saveOptions = new PdfSaveOptions();
// Bu belgeyi açan okuyucunun resimleri interpole etmesini sağlamak için "InterpolateImages" özelliğini "true" olarak ayarlayın.
// Çözünürlükleri, belgeyi görüntüleyen aygıtın çözünürlüğünden daha düşük olmalıdır.
// Okuyucunun herhangi bir enterpolasyon uygulamaması için "InterpolateImages" özelliğini "false" olarak ayarlayın.
saveOptions.InterpolateImages = interpolateImages;

// Bu belgeyi Adobe Acrobat gibi bir okuyucuyla açtığımızda, görüntüyü yakınlaştırmamız gerekecek
// Belgeyi enterpolasyon etkinken kaydedersek enterpolasyon etkisini görmek için.
doc.Save(ArtifactsDir + "PdfSaveOptions.InterpolateImages.pdf", saveOptions);
```

### Ayrıca bakınız

* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
