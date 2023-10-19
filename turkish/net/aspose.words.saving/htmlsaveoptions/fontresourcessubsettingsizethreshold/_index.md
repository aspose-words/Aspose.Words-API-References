---
title: HtmlSaveOptions.FontResourcesSubsettingSizeThreshold
linktitle: FontResourcesSubsettingSizeThreshold
articleTitle: FontResourcesSubsettingSizeThreshold
second_title: Aspose.Words for .NET
description: HtmlSaveOptions FontResourcesSubsettingSizeThreshold mülk. HTML MHTML veya EPUBa kaydederken hangi yazı tipi kaynaklarının alt ayarlamaya ihtiyaç duyduğunu kontrol eder. Varsayılan0  C#'da.
type: docs
weight: 290
url: /tr/net/aspose.words.saving/htmlsaveoptions/fontresourcessubsettingsizethreshold/
---
## HtmlSaveOptions.FontResourcesSubsettingSizeThreshold property

HTML, MHTML veya EPUB'a kaydederken hangi yazı tipi kaynaklarının alt ayarlamaya ihtiyaç duyduğunu kontrol eder. Varsayılan:`0` .

```csharp
public int FontResourcesSubsettingSizeThreshold { get; set; }
```

## Notlar

[`ExportFontResources`](../exportfontresources/) Yazı tiplerinin yardımcı dosyalar olarak veya çıktı paketinin parçaları olarak dışa aktarılmasına izin verir. Belgede çok sayıda yazı tipi kullanılıyorsa, özellikle de çok sayıda glif varsa, çıktı boyutu önemli ölçüde büyüyebilir . Yazı tipi alt kümesi, geçerli belge tarafından kullanılmayan gliflerini filtreleyerek dışa aktarılan yazı tipi kaynağının boyutunu azaltır.

Yazı tipi alt kümesi şu şekilde çalışır:

* Varsayılan olarak, dışa aktarılan tüm yazı tipleri alt kümelenir.
* Ayar`FontResourcesSubsettingSizeThreshold`pozitif bir değere Aspose.Words'e dosya boyutu belirtilen değerden büyük olan yazı tiplerini alt kümelemesi talimatını verir.
* Özelliğin şu şekilde ayarlanması:MaxValue yazı tipi alt kümelemesini bastırır.

**Önemli!** Yazı tipi kaynaklarını dışa aktarırken yazı tipi lisanslama sorunları dikkate alınmalıdır. Downloadable yazı tipi mekanizması aracılığıyla belirli yazı tiplerini kullanmak isteyen yazarların, kullanım amaçlarının yazı tipi lisansı kapsamında olduğunu her zaman dikkatli bir şekilde doğrulamaları gerekir. Pek çok ticari yazı tipi şu anda kendi yazı tiplerinin herhangi bir biçimde web'den indirilmesine izin vermemektedir. Bazı yazı tiplerini kapsayan lisans sözleşmeleri, özellikle şunu belirtir:**@yazı tipi yüzü** CSS stil sayfalarında Rules 'ye izin verilmiyor. Yazı tipi alt kümelemesi aynı zamanda lisans koşullarını da ihlal edebilir.

## Örnekler

Yazı tipi alt kümelemeyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Times New Roman";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("Hello world!");

// Belgeyi HTML'ye kaydettiğimizde, bir SaveOptions nesnesi yapılandırma yazı tipi alt kümesini iletebiliriz.
// "ExportFontResources" bayrağını "true" olarak ayarladığımızı ve ayrıca "FontsFolder" özelliğindeki bir klasörü adlandırdığımızı varsayalım.
// Bu durumda, kaydetme işlemi o klasörü oluşturacak ve içine bir .ttf dosyası yerleştirecektir.
// belgemizin kullandığı her yazı tipi için bu klasör.
// Her .ttf dosyası o yazı tipinin tüm glif setini içerecektir,
// bu muhtemelen belgeye eşlik eden çok büyük bir dosyayla sonuçlanabilir.
// Bir yazı tipine alt kümeleme uyguladığımızda, dışa aktarılan ham verileri yalnızca belgenin içerdiği glifleri içerecektir
// glif kümesinin tamamı yerine kullanılıyor. Belgemizdeki metinde bir yazı tipinin yalnızca küçük bir kısmı kullanılıyorsa
// glif ayarlandığında alt kümeleme çıktı belgelerimizin boyutunu önemli ölçüde azaltacaktır.
// Bayt cinsinden bir .ttf dosya boyutunu tanımlamak için "FontResourcesSubsettingSizeThreshold" özelliğini kullanabiliriz.
 // Dışa aktarılan bir yazı tipi bundan daha büyük boyutta bir dosya oluşturursa, kaydetme işlemi o yazı tipine alt kümeleme uygulayacaktır.
// 0 eşiğinin ayarlanması tüm yazı tiplerine alt kümeleme uygular,
// ve bunu "int.MaxValue" olarak ayarlamak, alt kümelemeyi etkili bir şekilde devre dışı bırakır.
string fontsFolder = ArtifactsDir + "HtmlSaveOptions.FontSubsetting.Fonts";

HtmlSaveOptions options = new HtmlSaveOptions
{
    ExportFontResources = true,
    FontsFolder = fontsFolder,
    FontResourcesSubsettingSizeThreshold = fontResourcesSubsettingSizeThreshold
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.FontSubsetting.html", options);

string[] fontFileNames = Directory.GetFiles(fontsFolder).Where(s => s.EndsWith(".ttf")).ToArray();

Assert.AreEqual(3, fontFileNames.Length);

foreach (string filename in fontFileNames)
{
    // Varsayılan olarak, üç yazı tipimizin her biri için .ttf dosyaları 700 MB'ın üzerinde olacaktır.
    // Alt kümeleme hepsini 30 MB'ın altına indirecektir.
    FileInfo fontFileInfo = new FileInfo(filename);

    Assert.True(fontFileInfo.Length > 700000 || fontFileInfo.Length < 30000);
    Assert.True(Math.Max(fontResourcesSubsettingSizeThreshold, 30000) > new FileInfo(filename).Length);
}
```

### Ayrıca bakınız

* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
