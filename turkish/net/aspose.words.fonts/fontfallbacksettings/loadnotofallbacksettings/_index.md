---
title: FontFallbackSettings.LoadNotoFallbackSettings
second_title: Aspose.Words for .NET API Referansı
description: FontFallbackSettings yöntem. Google Noto yazı tiplerini kullanan önceden tanımlanmış yedek ayarları yükler.
type: docs
weight: 40
url: /tr/net/aspose.words.fonts/fontfallbacksettings/loadnotofallbacksettings/
---
## FontFallbackSettings.LoadNotoFallbackSettings method

Google Noto yazı tiplerini kullanan önceden tanımlanmış yedek ayarları yükler.

```csharp
public void LoadNotoFallbackSettings()
```

### Örnekler

Google Noto yazı tipleri için önceden tanımlanmış yazı tipi yedek ayarlarının nasıl ekleneceğini gösterir.

```csharp
FontSettings fontSettings = new FontSettings();

// Bunlar, SIL Açık Yazı Tipi Lisansı altında lisanslanan ücretsiz yazı tipleridir.
// Fontları buradan indirebiliriz:
// https://www.google.com/get/noto/#sans-lgc
fontSettings.SetFontsFolder(FontsDir + "Noto", false);

 // Ön tanımlı ayarların yalnızca normal ağırlıklı Sans stili Noto yazı tiplerini kullandığını unutmayın.
// Noto yazı tiplerinden bazıları gelişmiş tipografi özelliklerini kullanır.
// Gelişmiş tipografiye sahip fontlar, Aspose.Words şu anda onları desteklemediğinden doğru şekilde oluşturulamayabilir.
fontSettings.FallbackSettings.LoadNotoFallbackSettings();
fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = false;
fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Noto Sans";

Document doc = new Document();
doc.FontSettings = fontSettings;
```

Önceden tanımlanmış yedek yazı tipi ayarlarının nasıl yükleneceğini gösterir.

```csharp
Document doc = new Document();

FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;
FontFallbackSettings fontFallbackSettings = fontSettings.FallbackSettings;

// Varsayılan yedek yazı tipi şemasını bir XML belgesine kaydedin.
// Örneğin, öğelerden biri Range için "0C00-0C7F" değerine ve FallbackFonts için karşılık gelen "Vani" değerine sahiptir.
// Bu, bazı metnin kullandığı yazı tipinin 0x0C00-0x0C7F Unicode bloğu için sembollere sahip olmadığı anlamına gelir.
// geri dönüş şeması, "Vani" yazı tipi yerine geçen sembolleri kullanacaktır.
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.Default.xml");

// Aşağıda, aralarından seçim yapabileceğimiz iki önceden tanımlanmış yazı tipi geri dönüş şeması bulunmaktadır.
// 1 - Varsayılanla aynı olan varsayılan Microsoft Office şemasını kullanın:
fontFallbackSettings.LoadMsOfficeFallbackSettings();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.LoadMsOfficeFallbackSettings.xml");

// 2 - Google Noto yazı tiplerinden oluşturulmuş şemayı kullanın:
fontFallbackSettings.LoadNotoFallbackSettings();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.LoadNotoFallbackSettings.xml");
```

### Ayrıca bakınız

* class [FontFallbackSettings](../)
* ad alanı [Aspose.Words.Fonts](../../fontfallbacksettings/)
* toplantı [Aspose.Words](../../../)


