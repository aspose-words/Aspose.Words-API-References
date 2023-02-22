---
title: Class FontFallbackSettings
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Fonts.FontFallbackSettings sınıf. Yazı tipi geri dönüş mekanizması ayarlarını belirtir.
type: docs
weight: 2720
url: /tr/net/aspose.words.fonts/fontfallbacksettings/
---
## FontFallbackSettings class

Yazı tipi geri dönüş mekanizması ayarlarını belirtir.

```csharp
public class FontFallbackSettings
```

## yöntemler

| İsim | Tanım |
| --- | --- |
| [BuildAutomatic](../../aspose.words.fonts/fontfallbacksettings/buildautomatic/)() | Kullanılabilir yazı tiplerini tarayarak yedek ayarları otomatik olarak oluşturur. |
| [Load](../../aspose.words.fonts/fontfallbacksettings/load/#load)(Stream) | XML akışından yedek ayarları yükler. |
| [Load](../../aspose.words.fonts/fontfallbacksettings/load/#load_1)(string) | XML dosyasından yazı tipi yedek ayarlarını yükler. |
| [LoadMsOfficeFallbackSettings](../../aspose.words.fonts/fontfallbacksettings/loadmsofficefallbacksettings/)() | Microsoft Word yedeğini taklit eden ve Microsoft ofis yazı tiplerini kullanan önceden tanımlanmış geri dönüş ayarlarını yükler. |
| [LoadNotoFallbackSettings](../../aspose.words.fonts/fontfallbacksettings/loadnotofallbacksettings/)() | Google Noto yazı tiplerini kullanan önceden tanımlanmış yedek ayarları yükler. |
| [Save](../../aspose.words.fonts/fontfallbacksettings/save/#save)(Stream) | Mevcut yedek ayarları akışa kaydeder. |
| [Save](../../aspose.words.fonts/fontfallbacksettings/save/#save_1)(string) | Geçerli geri dönüş ayarlarını dosyaya kaydeder. |

### Notlar

Varsayılan olarak yedek ayarlar, Microsoft Word geri dönüşünü taklit eden önceden tanımlanmış ayarlarla başlatılır.

### Örnekler

Unicode karakter kod aralıkları arasında yedek yazı tiplerinin nasıl dağıtılacağını gösterir.

```csharp
Document doc = new Document();

FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;
FontFallbackSettings fontFallbackSettings = fontSettings.FallbackSettings;

// Font ayarlarımızı sadece "MyFonts" klasöründen fontları kaynaklayacak şekilde yapılandırın.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
fontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

// "BuildAutomatic" yöntemini çağırmak, bir geri dönüş şeması oluşturacaktır.
// erişilebilir yazı tiplerini mümkün olduğu kadar çok Unicode karakter koduna dağıtır.
// Bizim durumumuzda, "MyFonts" klasörü içindeki yalnızca bir avuç yazı tipine erişimi vardır.
fontFallbackSettings.BuildAutomatic();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettingsCustom.BuildAutomatic.xml");

// Bunun gibi bir dosyadan özel bir ikame şeması da yükleyebiliriz.
// Bu şema, "0000-00ff" Unicode blokları boyunca "AllegroOpen" yazı tipini, "0100-024f" boyunca "AllegroOpen" yazı tipini uygular,
// ve şemadaki diğer yazı tiplerinin kapsamadığı diğer tüm aralıklardaki "M+ 2m" yazı tipi.
fontFallbackSettings.Load(MyDir + "Custom font fallback settings.xml");

// Bir belge oluşturucu oluşturun ve yazı tipini hiçbir kaynağımızda bulunmayan bir yazı tipine ayarlayın.
// Yazı tipi ayarlarımız, mevcut olmayan yazı tipini kullanarak yazdığımız karakterler için geri dönüş şemasını çağıracaktır.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Missing Font";

// 0x0021'den 0x052F'ye kadar her Unicode karakterini yazdırmak için oluşturucuyu kullanın,
// özel yazı tipi geri dönüş şemamızda tanımladığımız Unicode bloklarını bölen açıklayıcı çizgilerle.
for (int i = 0x0021; i < 0x0530; i++)
{
    switch (i)
    {
        case 0x0021:
            builder.Writeln(
                "\n\n0x0021 - 0x00FF: \nBasic Latin/Latin-1 Supplement Unicode blocks in \"AllegroOpen\" font:");
            break;
        case 0x0100:
            builder.Writeln(
                "\n\n0x0100 - 0x024F: \nLatin Extended A/B blocks, mostly in \"AllegroOpen\" font:");
            break;
        case 0x0250:
            builder.Writeln("\n\n0x0250 - 0x052F: \nIPA/Greek/Cyrillic blocks in \"M+ 2m\" font:");
            break;
    }

    builder.Write($"{Convert.ToChar(i)}");
}

doc.Save(ArtifactsDir + "FontSettings.FallbackSettingsCustom.pdf");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Fonts](../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../)


