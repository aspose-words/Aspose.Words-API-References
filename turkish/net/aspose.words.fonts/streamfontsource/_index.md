---
title: StreamFontSource Class
linktitle: StreamFontSource
articleTitle: StreamFontSource
second_title: .NET için Aspose.Words
description: Belge esnekliğini ve tasarımını geliştiren özel akış yazı tipi kaynakları için başvuracağınız çözüm olan Aspose.Words.Fonts.StreamFontSource sınıfını keşfedin.
type: docs
weight: 3470
url: /tr/net/aspose.words.fonts/streamfontsource/
---
## StreamFontSource class

Kullanıcı tanımlı akış yazı tipi kaynağı için temel sınıf.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Yazı Tipleriyle Çalışma](https://docs.aspose.com/words/net/working-with-fonts/) belgeleme makalesi.

```csharp
public abstract class StreamFontSource : FontSourceBase,   
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CacheKey](../../aspose.words.fonts/streamfontsource/cachekey/) { get; } | Önbellekteki bu kaynağın anahtarı. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Yazı tipi kaynak önceliğini döndürür. |
| [Type](../../aspose.words.fonts/streamfontsource/type/) { get; } | Yazı tipi kaynağının türünü döndürür. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Biçimlendirme sadakat kaybına yol açabilecek bir sorun algılandığında yazı tipi kaynağının işlenmesi sırasında çağrılır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Bu kaynak aracılığıyla kullanılabilir yazı tiplerinin listesini döndürür. |
| abstract [OpenFontDataStream](../../aspose.words.fonts/streamfontsource/openfontdatastream/)() | Bu yöntem, akışı talep üzerine yazı tipi verileriyle açmalıdır. |

## Notlar

Akış yazı tipi kaynağını kullanmak için, akış yazı tipi kaynağından türetilmiş bir sınıf oluşturmalısınız.`StreamFontSource` ve uygulamasını sağlayın[`OpenFontDataStream`](./openfontdatastream/) yöntem.

[`OpenFontDataStream`](./openfontdatastream/)yöntem birkaç kez çağrılabilir. İlk kez, Aspose.Words mevcut fontların listesini almak için sağlanan font kaynaklarını taradığında çağrılacaktır. Daha sonra, font verilerini ayrıştırmak ve font verilerini bazı çıktı biçimlerine yerleştirmek için belgede fontu kullanılırsa çağrılabilir.

`StreamFontSource` yararlı olabilir çünkü yazı tipi verilerinin yalnızca gerektiğinde yüklenmesine izin verir ve bellekte saklanmasına izin vermez[`FontSettings`](../fontsettings/) ömür boyu.

## Örnekler

Yazı tiplerinin akıştan nasıl yükleneceğini gösterir.

```csharp
public void StreamFontSourceFileRendering()
{
    FontSettings fontSettings = new FontSettings();
    fontSettings.SetFontsSources(new FontSourceBase[] {new StreamFontSourceFile()});

    DocumentBuilder builder = new DocumentBuilder();
    builder.Document.FontSettings = fontSettings;
    builder.Font.Name = "Kreon-Regular";
    builder.Writeln("Test aspose text when saving to PDF.");

    builder.Document.Save(ArtifactsDir + "FontSettings.StreamFontSourceFileRendering.pdf");
}

/// <summary>
/// Font verilerini hafızada saklamak yerine yalnızca gerektiğinde yükleyin
/// "FontSettings" nesnesinin tüm yaşam süresi boyunca.
/// </summary>
private class StreamFontSourceFile : StreamFontSource
{
    public override Stream OpenFontDataStream()
    {
        return File.OpenRead(FontsDir + "Kreon-Regular.ttf");
    }
}
```

### Ayrıca bakınız

* class [FontSourceBase](../fontsourcebase/)
* interface [  ](../../global/%02  /)
* ad alanı [Aspose.Words.Fonts](../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../)
