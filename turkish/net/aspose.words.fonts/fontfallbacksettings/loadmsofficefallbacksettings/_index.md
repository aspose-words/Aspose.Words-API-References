---
title: FontFallbackSettings.LoadMsOfficeFallbackSettings
linktitle: LoadMsOfficeFallbackSettings
articleTitle: LoadMsOfficeFallbackSettings
second_title: Aspose.Words for .NET
description: FontFallbackSettings LoadMsOfficeFallbackSettings yöntem. Microsoft Word geri dönüşünü taklit eden ve Microsoft Office yazı tiplerini kullanan önceden tanımlanmış geri dönüş ayarlarını yükler C#'da.
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

// Varsayılan geri dönüş yazı tipi düzenini bir XML belgesine kaydedin.
// Örneğin, öğelerden biri Range için "0C00-0C7F" değerine ve FallbackFonts için buna karşılık gelen "Vani" değerine sahiptir.
// Bu, bazı metinlerin kullandığı yazı tipinin 0x0C00-0x0C7F Unicode bloğu için sembollere sahip olmadığı anlamına gelir.
// geri dönüş şeması "Vani" yazı tipi yerine geçen sembolleri kullanacaktır.
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.Default.xml");

// Aşağıda aralarından seçim yapabileceğimiz önceden tanımlanmış iki yazı tipi geri dönüş şeması bulunmaktadır.
// 1 - Varsayılanla aynı olan varsayılan Microsoft Office şemasını kullanın:
fontFallbackSettings.LoadMsOfficeFallbackSettings();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.LoadMsOfficeFallbackSettings.xml");

// 2 - Google Noto yazı tiplerinden oluşturulan şemayı kullanın:
fontFallbackSettings.LoadNotoFallbackSettings();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.LoadNotoFallbackSettings.xml");
```

### Ayrıca bakınız

* class [FontFallbackSettings](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)
