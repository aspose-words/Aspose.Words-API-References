---
title: FontFallbackSettings.LoadNotoFallbackSettings
linktitle: LoadNotoFallbackSettings
articleTitle: LoadNotoFallbackSettings
second_title: .NET için Aspose.Words
description: Google Noto yazı tiplerini kullanarak kusursuz metin gösterimi için FontFallbackSettings LoadNotoFallbackSettings yöntemiyle tipografinizi nasıl geliştirebileceğinizi keşfedin.
type: docs
weight: 40
url: /tr/net/aspose.words.fonts/fontfallbacksettings/loadnotofallbacksettings/
---
## FontFallbackSettings.LoadNotoFallbackSettings method

Google Noto yazı tiplerini kullanan önceden tanımlanmış yedek ayarları yükler.

```csharp
public void LoadNotoFallbackSettings()
```

## Örnekler

Google Noto yazı tipleri için önceden tanımlanmış yazı tipi yedek ayarlarının nasıl ekleneceğini gösterir.

```csharp
FontSettings fontSettings = new FontSettings();

// Bunlar SIL Açık Font Lisansı altında lisanslanan ücretsiz fontlardır.
// Fontları buradan indirebiliriz:
// https://www.google.com/get/noto/#sans-lgc
fontSettings.SetFontsFolder(FontsDir + "Noto", false);

 // Önceden tanımlanmış ayarların yalnızca normal ağırlığa sahip Sans tarzı Noto yazı tiplerini kullandığını unutmayın.
// Noto yazı tiplerinin bazıları gelişmiş tipografi özelliklerini kullanır.
// Gelişmiş tipografiye sahip yazı tipleri, Aspose.Words tarafından şu anda desteklenmediği için doğru şekilde işlenmeyebilir.
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
// Örneğin, öğelerden birinin Range değeri "0C00-0C7F" ve FallbackFonts değeri de buna karşılık gelen "Vani"dir.
// Bu, bazı metinlerin kullandığı yazı tipinin 0x0C00-0x0C7F Unicode bloğu için semboller içermemesi anlamına gelir,
// yedek şema "Vani" yazı tipi yerine kullanılan sembolleri kullanacaktır.
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.Default.xml");

// Aşağıda seçebileceğimiz iki önceden tanımlanmış yazı tipi geri dönüş şeması bulunmaktadır.
// 1 - Varsayılanla aynı olan varsayılan Microsoft Office şemasını kullanın:
fontFallbackSettings.LoadMsOfficeFallbackSettings();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.LoadMsOfficeFallbackSettings.xml");

// 2 - Google Noto fontlarından oluşturulan şemayı kullanın:
fontFallbackSettings.LoadNotoFallbackSettings();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.LoadNotoFallbackSettings.xml");
```

### Ayrıca bakınız

* class [FontFallbackSettings](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)
