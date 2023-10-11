---
title: HtmlSaveOptions.ScaleImageToShapeSize
second_title: Aspose.Words for .NET API Referansı
description: HtmlSaveOptions mülk. Görüntülerin HTML MHTML veya EPUBa aktarılırken Aspose.Words tarafından sınırlayıcı şekil boyutuna ölçeklenip ölçeklenmeyeceğini belirtir. Varsayılan değerdoğru .
type: docs
weight: 450
url: /tr/net/aspose.words.saving/htmlsaveoptions/scaleimagetoshapesize/
---
## HtmlSaveOptions.ScaleImageToShapeSize property

Görüntülerin HTML, MHTML veya EPUB'a aktarılırken Aspose.Words tarafından sınırlayıcı şekil boyutuna ölçeklenip ölçeklenmeyeceğini belirtir. Varsayılan değer:`doğru` .

```csharp
public bool ScaleImageToShapeSize { get; set; }
```

### Notlar

Microsoft Word belgesindeki görüntü bir şekildir. Şeklin bir boyutu vardır ve image 'nin kendi boyutu vardır. Boyutlar doğrudan bağlantılı değildir. Örneğin görsel 1024x786 piksel, olabilir ama bu görseli gösteren şekil 400x300 punto olabilir.

Bir resmin tarayıcıda görüntülenmesi için şekil boyutuna göre ölçeklendirilmesi gerekir. `ScaleImageToShapeSize` özellik, image 'nin ölçeklendirmesinin nerede gerçekleşeceğini kontrol eder: HTML'ye aktarma sırasında Aspose.Words'te veya belgeyi görüntülerken tarayıcıda.

Ne zaman`ScaleImageToShapeSize` dır-dir`doğru` görüntü, HTML'ye aktarım sırasında yüksek kaliteli ölçeklendirme kullanılarak Aspose.Words tarafından ölçeklendirilir. Ne zaman`ScaleImageToShapeSize` :`YANLIŞ`, görüntü orijinal boyutunda çıkarılır ve tarayıcının onu ölçeklendirmesi gerekir.

Genel olarak tarayıcılar hızlı ve kalitesiz ölçeklendirme yaparlar. Sonuç olarak, normalde tarayıcıda daha iyi görüntü kalitesi elde edersiniz ve dosya boyutunu küçültürsünüz.`ScaleImageToShapeSize` dır-dir`doğru` , ancak daha iyi baskı kalitesi ve daha hızlı dönüşüm`ScaleImageToShapeSize` dır-dir`YANLIŞ`.

Bu seçenek, ayrı tarama görüntüleri içeren şekillere ek olarak, x000d_ tarama görüntülerinden oluşan grup şekillerini de etkiler. Eğer`ScaleImageToShapeSize` dır-dir`YANLIŞ` ve bir grup şekli, içsel çözünürlüğü belirtilen değerden daha yüksek olan raster görüntüler içerir[`ImageResolution`](../imageresolution/), Aspose.Words bu grup için görüntü oluşturma çözünürlüğünü artıracaktır. Bu, HTML'ye kaydederken gruplandırılmış yüksek çözünürlüklü görüntülerin kalitesinin daha iyi korunmasına olanak tanır.

### Örnekler

.html'ye kaydederken görüntülerin üst şekil boyutlarına ölçeklendirilmesinin nasıl devre dışı bırakılacağını gösterir.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            // Resim içeren bir şekil ekleyin ve ardından bu şekli resimden oldukça küçük yapın.
#if NET48 || JAVA
            Image image = Image.FromFile(ImageDir + "Transparent background logo.png");

            Assert.AreEqual(400, image.Size.Width);
            Assert.AreEqual(400, image.Size.Height);
#elif NET5_0_OR_GREATER
            SKBitmap image = SKBitmap.Decode(ImageDir + "Transparent background logo.png");

            Assert.AreEqual(400, image.Width);
            Assert.AreEqual(400, image.Height);
#endif

            Shape imageShape = builder.InsertImage(image);
            imageShape.Width = 50;
            imageShape.Height = 50;

            // Resim içeren şekiller içeren bir belgenin HTML'ye kaydedilmesi, yerel dosya sisteminde bir resim dosyası oluşturacaktır
            // bu tür her şekil için. Çıktı HTML belgesinde <image> Bu görsellere bağlanmak ve bunları görüntülemek için etiketler kullanın.
            // Belgeyi HTML'ye kaydettiğimizde, belirlemek için bir SaveOptions nesnesini iletebiliriz.
            // şekillerin içindeki tüm görsellerin şekillerin boyutlarına göre ölçeklenip ölçeklenmeyeceği.
            // "ScaleImageToShapeSize" bayrağını "true" olarak ayarlamak her resmi küçültecektir
            // onu içeren şeklin boyutuna değiştir, böylece kaydedilen hiçbir görüntü belgenin gerektirdiğinden daha büyük olmayacaktır.
            // "ScaleImageToShapeSize" bayrağını "false" olarak ayarlamak bu görsellerin orijinal boyutlarını koruyacaktır,
            // görüntü kalitesinin korunması karşılığında daha fazla yer kaplayacak.
            HtmlSaveOptions options = new HtmlSaveOptions { ScaleImageToShapeSize = scaleImageToShapeSize };

            doc.Save(ArtifactsDir + "HtmlSaveOptions.ScaleImageToShapeSize.html", options);

            FileInfo fileInfo = new FileInfo(ArtifactsDir + "HtmlSaveOptions.ScaleImageToShapeSize.001.png");

#if NET48 || JAVA
        if (scaleImageToShapeSize)
            Assert.That(3000, Is.AtLeast(fileInfo.Length));
        else
            Assert.That(20000, Is.LessThan(fileInfo.Length));
#elif NET5_0_OR_GREATER
        if (scaleImageToShapeSize)
            Assert.That(10000, Is.AtLeast(fileInfo.Length));
        else
            Assert.That(30000, Is.LessThan(fileInfo.Length));
#endif
```

### Ayrıca bakınız

* property [ImageResolution](../imageresolution/)
* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../htmlsaveoptions/)
* toplantı [Aspose.Words](../../../)


