---
title: FontFallbackSettings.LoadMsOfficeFallbackSettings
linktitle: LoadMsOfficeFallbackSettings
articleTitle: LoadMsOfficeFallbackSettings
second_title: .NET için Aspose.Words
description: Sorunsuz entegrasyon için Microsoft Word benzeri geri dönüş ayarlarını Office yazı tipleriyle kolayca uygulamak üzere FontFallbackSettings LoadMsOfficeFallbackSettings yöntemini keşfedin.
type: docs
weight: 30
url: /tr/net/aspose.words.fonts/fontfallbacksettings/loadmsofficefallbacksettings/
---
## FontFallbackSettings.LoadMsOfficeFallbackSettings method

Microsoft Word geri dönüşünü taklit eden ve Microsoft Office yazı tiplerini kullanan önceden tanımlanmış geri dönüş ayarlarını yükler.

```csharp
public void LoadMsOfficeFallbackSettings()
```

## Örnekler

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
