---
title: FontSettings.FallbackSettings
linktitle: FallbackSettings
articleTitle: FallbackSettings
second_title: .NET için Aspose.Words
description: Optimize edilmiş font geri dönüş mekanizmaları için FontSettings FallbackSettings özelliğini keşfedin. Tasarımınızı kusursuz metin işlemeyle geliştirin!
type: docs
weight: 30
url: /tr/net/aspose.words.fonts/fontsettings/fallbacksettings/
---
## FontSettings.FallbackSettings property

Yazı tipi geri dönüş mekanizmasıyla ilgili ayarlar.

```csharp
public FontFallbackSettings FallbackSettings { get; }
```

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

* class [FontFallbackSettings](../../fontfallbacksettings/)
* class [FontSettings](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)
