---
title: HtmlSaveOptions.ScaleImageToShapeSize
linktitle: ScaleImageToShapeSize
articleTitle: ScaleImageToShapeSize
second_title: .NET için Aspose.Words
description: HtmlSaveOptions' ScaleImageToShapeSize özelliğinin Aspose.Words'de HTML, MHTML veya EPUB dışa aktarımları için görüntü ölçeklemesini nasıl optimize ettiğini keşfedin. Belgelerinizi geliştirin!
type: docs
weight: 470
url: /tr/net/aspose.words.saving/htmlsaveoptions/scaleimagetoshapesize/
---
## HtmlSaveOptions.ScaleImageToShapeSize property

HTML, MHTML veya EPUB'a aktarırken görüntülerin Aspose.Words tarafından sınırlayıcı şekil boyutuna ölçeklenip ölçeklenmeyeceğini belirtir. Varsayılan değer`doğru` .

```csharp
public bool ScaleImageToShapeSize { get; set; }
```

## Notlar

Microsoft Word belgesindeki bir resim bir şekildir. Şeklin bir boyutu vardır ve image kendi boyutuna sahiptir. Boyutlar doğrudan bağlantılı değildir. Örneğin, resim 1024x786 piksel olabilir, ancak bu resmi görüntüleyen şekil 400x300 nokta olabilir.

Bir görüntüyü tarayıcıda görüntülemek için, şeklin boyutuna ölçeklendirilmesi gerekir. `ScaleImageToShapeSize` özellik, image ölçeklemesinin nerede gerçekleştiğini kontrol eder: HTML'ye aktarma sırasında Aspose.Words'de veya belge görüntülenirken tarayıcıda.

Ne zaman`ScaleImageToShapeSize` dır`doğru` , görüntü HTML'ye aktarma sırasında yüksek kaliteli ölçekleme kullanılarak Aspose.Words tarafından ölçeklendirilir.`ScaleImageToShapeSize` şudur`YANLIŞ`, görüntü orijinal boyutuyla çıktılanır ve tarayıcının onu ölçeklemesi gerekir.

Genel olarak, tarayıcılar hızlı ve düşük kaliteli ölçekleme yapar. Sonuç olarak, tarayıcıda normalde daha iyi görüntüleme kalitesi ve daha küçük dosya boyutu elde edersiniz.`ScaleImageToShapeSize` dır`doğru` , ancak daha iyi baskı kalitesi ve daha hızlı dönüşüm`ScaleImageToShapeSize` dır`YANLIŞ`.

Bireysel raster görüntüleri içeren şekillere ek olarak, bu seçenek ayrıca raster görüntülerden oluşan grup şekillerini de etkiler.`ScaleImageToShapeSize` dır`YANLIŞ` ve bir grup şekli, içsel çözünürlüğü belirtilen değerden daha yüksek olan raster images içerir[`ImageResolution`](../imageresolution/), Aspose.Words bu grup için işleme çözünürlüğünü artıracaktır. Bu, HTML'ye kaydederken gruplanmış yüksek çözünürlüklü görüntülerin kalitesinin daha iyi korunmasını sağlar.

## Örnekler

.html'ye kaydederken görüntülerin ana şekil boyutlarına ölçeklenmesinin nasıl devre dışı bırakılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// İçinde resim bulunan bir şekil ekle ve sonra o şekli resimden önemli ölçüde daha küçük yap.
Shape imageShape = builder.InsertImage(ImageDir + "Transparent background logo.png");
imageShape.Width = 50;
imageShape.Height = 50;

// Resimlerle birlikte şekiller içeren bir belgeyi HTML'ye kaydetmek, yerel dosya sisteminde bir resim dosyası oluşturacaktır
// bu tür her şekil için. Çıktı HTML belgesi, bu resimlere bağlanmak ve onları görüntülemek için <image> etiketlerini kullanacaktır.
// Belgeyi HTML'e kaydettiğimizde, SaveOptions nesnesini belirlemek için bir SaveOptions nesnesi geçirebiliriz.
// şekillerin içindeki tüm görsellerin şekillerinin boyutlarına ölçeklenip ölçeklenmeyeceği.
// "ScaleImageToShapeSize" bayrağını "true" olarak ayarlamak her resmi küçültecektir
// kendisini içeren şeklin boyutuna göre, böylece kaydedilen hiçbir görüntü belgenin gerektirdiğinden daha büyük olmayacaktır.
// "ScaleImageToShapeSize" bayrağını "false" olarak ayarlamak bu resimlerin orijinal boyutlarını koruyacaktır.
// görüntü kalitesinin korunması karşılığında daha fazla yer kaplayacak.
HtmlSaveOptions options = new HtmlSaveOptions { ScaleImageToShapeSize = scaleImageToShapeSize };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ScaleImageToShapeSize.html", options);
```

### Ayrıca bakınız

* property [ImageResolution](../imageresolution/)
* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
