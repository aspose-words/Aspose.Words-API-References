---
title: FontFallbackSettings Class
linktitle: FontFallbackSettings
articleTitle: FontFallbackSettings
second_title: .NET için Aspose.Words
description: Özelleştirilebilir yazı tipi geri dönüş seçenekleri için Aspose.Words.Fonts.FontFallbackSettings'i keşfedin; kusursuz belge oluşturma ve gelişmiş metin görüntülemesi sağlayın.
type: docs
weight: 3330
url: /tr/net/aspose.words.fonts/fontfallbacksettings/
---
## FontFallbackSettings class

Yazı tipi geri dönüş mekanizması ayarlarını belirtir.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Yazı Tipleriyle Çalışma](https://docs.aspose.com/words/net/working-with-fonts/) belgeleme makalesi.

```csharp
public class FontFallbackSettings
```

## yöntemler

| İsim | Tanım |
| --- | --- |
| [BuildAutomatic](../../aspose.words.fonts/fontfallbacksettings/buildautomatic/)() | Mevcut yazı tiplerini tarayarak otomatik olarak yedek ayarları oluşturur. |
| [Load](../../aspose.words.fonts/fontfallbacksettings/load/#load)(*Stream*) | XML akışından yedek ayarları yükler. |
| [Load](../../aspose.words.fonts/fontfallbacksettings/load/#load_1)(*string*) | XML dosyasından yazı tipi yedek ayarlarını yükler. |
| [LoadMsOfficeFallbackSettings](../../aspose.words.fonts/fontfallbacksettings/loadmsofficefallbacksettings/)() | Microsoft Word geri dönüşünü taklit eden ve Microsoft Office yazı tiplerini kullanan önceden tanımlanmış geri dönüş ayarlarını yükler. |
| [LoadNotoFallbackSettings](../../aspose.words.fonts/fontfallbacksettings/loadnotofallbacksettings/)() | Google Noto yazı tiplerini kullanan önceden tanımlanmış yedek ayarları yükler. |
| [Save](../../aspose.words.fonts/fontfallbacksettings/save/#save)(*Stream*) | Mevcut yedek ayarları akışa kaydeder. |
| [Save](../../aspose.words.fonts/fontfallbacksettings/save/#save_1)(*string*) | Mevcut geri dönüş ayarlarını dosyaya kaydeder. |

## Notlar

Varsayılan olarak, geri dönüş ayarları Microsoft Word geri dönüşünü taklit eden önceden tanımlanmış ayarlarla başlatılır.

## Örnekler

Yedek yazı tiplerinin Unicode karakter kodu aralıkları arasında nasıl dağıtılacağını gösterir.

```csharp
Document doc = new Document();

FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;
FontFallbackSettings fontFallbackSettings = fontSettings.FallbackSettings;

// Font ayarlarımızı yalnızca "MyFonts" klasöründen font alacak şekilde yapılandıralım.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
fontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

// "BuildAutomatic" yöntemini çağırmak, bir geri dönüş şeması oluşturacaktır.
// Erişilebilir yazı tiplerini mümkün olduğunca çok sayıda Unicode karakter koduna dağıtır.
// Bizim durumumuzda, yalnızca "MyFonts" klasöründeki bir avuç yazı tipine erişimi var.
fontFallbackSettings.BuildAutomatic();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettingsCustom.BuildAutomatic.xml");

// Bu şekilde bir dosyadan özel bir ikame şeması da yükleyebiliriz.
// Bu şema "0000-00ff" Unicode blokları boyunca "AllegroOpen" yazı tipini, "0100-024f" boyunca "AllegroOpen" yazı tipini uygular.
// ve şema içindeki diğer fontların kapsamadığı tüm diğer aralıklardaki "M+ 2m" fontu.
fontFallbackSettings.Load(MyDir + "Custom font fallback settings.xml");

// Bir belge oluşturucu oluşturun ve yazı tipini kaynaklarımızda bulunmayan bir yazı tipine ayarlayın.
// Yazı tipi ayarlarımız, mevcut olmayan yazı tipini kullanarak yazdığımız karakterler için yedek şemayı çağıracaktır.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Missing Font";

// 0x0021'den 0x052F'ye kadar her Unicode karakterini yazdırmak için oluşturucuyu kullanın,
// özel yazı tipi yedekleme şemalarımızda tanımladığımız Unicode bloklarını ayıran açıklayıcı çizgilerle.
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
