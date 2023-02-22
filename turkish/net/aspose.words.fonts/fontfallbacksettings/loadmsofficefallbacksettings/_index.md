---
title: FontFallbackSettings.LoadMsOfficeFallbackSettings
second_title: Aspose.Words for .NET API Referansı
description: FontFallbackSettings yöntem. Microsoft Word yedeğini taklit eden ve Microsoft ofis yazı tiplerini kullanan önceden tanımlanmış geri dönüş ayarlarını yükler.
type: docs
weight: 30
url: /tr/net/aspose.words.fonts/fontfallbacksettings/loadmsofficefallbacksettings/
---
## FontFallbackSettings.LoadMsOfficeFallbackSettings method

Microsoft Word yedeğini taklit eden ve Microsoft ofis yazı tiplerini kullanan önceden tanımlanmış geri dönüş ayarlarını yükler.

```csharp
public void LoadMsOfficeFallbackSettings()
```

### Örnekler

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


