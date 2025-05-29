---
title: HtmlSaveOptions.FontResourcesSubsettingSizeThreshold
linktitle: FontResourcesSubsettingSizeThreshold
articleTitle: FontResourcesSubsettingSizeThreshold
second_title: .NET için Aspose.Words
description: FontResourcesSubsettingSizeThreshold özelliğiyle HTML, MHTML veya EPUB dosyalarınızı optimize ederek verimli font kaynak yönetimi sağlayın. Varsayılan, 0.
type: docs
weight: 290
url: /tr/net/aspose.words.saving/htmlsaveoptions/fontresourcessubsettingsizethreshold/
---
## HtmlSaveOptions.FontResourcesSubsettingSizeThreshold property

HTML, MHTML veya EPUB'a kaydederken hangi yazı tipi kaynaklarının alt kümeye ayrılması gerektiğini kontrol eder. Varsayılan`0` .

```csharp
public int FontResourcesSubsettingSizeThreshold { get; set; }
```

## Notlar

[`ExportFontResources`](../exportfontresources/) fontların yardımcı dosyalar veya output paketinin parçaları olarak dışa aktarılmasına izin verir. Belge çok sayıda font kullanıyorsa, özellikle çok sayıda glif varsa, çıktı boyutu önemli ölçüde büyüyebilir . Font alt kümelemesi, geçerli belge tarafından kullanılmayan glifleri filtreleyerek dışa aktarılan font kaynağının boyutunu azaltır.

Yazı tipi alt kümelemesi şu şekilde çalışır:

* Varsayılan olarak, dışa aktarılan tüm yazı tipleri alt kümeye ayrılır.
* Ayar`FontResourcesSubsettingSizeThreshold` pozitif bir değere Aspose.Words'e dosya boyutu belirtilen değerden büyük olan yazı tiplerini alt kümeye ayırmasını söyler.
* Özelliği şu şekilde ayarlayın:MaxValue yazı tipi alt kümelemesini bastırır.

**Önemli!**Font kaynaklarını dışa aktarırken, font lisanslama sorunları dikkate alınmalıdır. Belirli fontları downloadable font mekanizması aracılığıyla kullanmak isteyen yazarlar, amaçlanan kullanımlarının font lisansının kapsamında olduğundan her zaman dikkatlice emin olmalıdır. Birçok ticari font şu anda fontlarının herhangi bir biçimde web üzerinden indirilmesine izin vermemektedir. Bazı fontları kapsayan lisans sözleşmeleri, özellikle kullanımın**@yazı-yüzü** CSS stil sayfalarında rules izin verilmez. Yazı tipi alt kümelemesi de lisans koşullarını ihlal edebilir.

## Örnekler

Yazı tipi alt kümelemesinin nasıl yapılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Times New Roman";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("Hello world!");

// Belgeyi HTML'e kaydettiğimizde, yazı tipi alt kümelerini yapılandırmak için bir SaveOptions nesnesi geçirebiliriz.
// "ExportFontResources" bayrağını "true" olarak ayarladığımızı ve ayrıca "FontsFolder" özelliğinde bir klasöre isim verdiğimizi varsayalım.
// Bu durumda, kaydetme işlemi bu klasörü oluşturacak ve içine bir .ttf dosyası yerleştirecektir.
// belgemizin kullandığı her yazı tipi için klasör.
// Her .ttf dosyası o yazı tipinin tüm glif setini içerecektir,
// bu da belgeye eşlik eden çok büyük bir dosyanın oluşmasına neden olabilir.
// Bir yazı tipine alt kümeleme uyguladığımızda, dışa aktarılan ham verileri yalnızca belgenin içerdiği glifleri içerecektir.
// tüm glif kümesi yerine kullanılır. Belgemizdeki metin bir fontun yalnızca küçük bir kısmını kullanıyorsa
// glif kümesini ayarladıktan sonra alt kümeleme yapmak çıktı belgelerimizin boyutunu önemli ölçüde azaltacaktır.
// .ttf dosya boyutunu bayt cinsinden tanımlamak için "FontResourcesSubsettingSizeThreshold" özelliğini kullanabiliriz.
 // Eğer dışa aktarılan bir yazı tipi bundan daha büyük boyutlu bir dosya oluşturursa, kaydetme işlemi alt kümelemeyi o yazı tipine uygulayacaktır.
// 0 eşik değeri ayarlandığında, alt kümeleme tüm yazı tiplerine uygulanır,
// ve bunu "int.MaxValue" olarak ayarlamak alt kümelemeyi etkin bir şekilde devre dışı bırakır.
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
    // Varsayılan olarak, üç yazı tipimizin her birinin .ttf dosyaları 700 MB'ın üzerinde olacaktır.
    // Alt kümeleme hepsini 30 MB'ın altına düşürecektir.
    FileInfo fontFileInfo = new FileInfo(filename);

    Assert.True(fontFileInfo.Length > 700000 || fontFileInfo.Length < 30000);
    Assert.True(Math.Max(fontResourcesSubsettingSizeThreshold, 30000) > new FileInfo(filename).Length);
}
```

### Ayrıca bakınız

* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
