---
title: StreamFontSource Class
linktitle: StreamFontSource
articleTitle: StreamFontSource
second_title: Aspose.Words for .NET
description: Aspose.Words.Fonts.StreamFontSource sınıf. Kullanıcı tanımlı akış yazı tipi kaynağı için temel sınıf C#'da.
type: docs
weight: 3040
url: /tr/net/aspose.words.fonts/streamfontsource/
---
## StreamFontSource class

Kullanıcı tanımlı akış yazı tipi kaynağı için temel sınıf.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Fontlarla Çalışmak](https://docs.aspose.com/words/net/working-with-fonts/) dokümantasyon makalesi.

```csharp
public abstract class StreamFontSource : FontSourceBase
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CacheKey](../../aspose.words.fonts/streamfontsource/cachekey/) { get; } | Bu kaynağın önbellekteki anahtarı. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Yazı tipi kaynağı önceliğini döndürür. |
| [Type](../../aspose.words.fonts/streamfontsource/type/) { get; } | Yazı tipi kaynağının türünü döndürür. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Yazı tipi kaynağının işlenmesi sırasında, biçimlendirmenin aslına uygunluk kaybına yol açabilecek bir sorun algılandığında çağrılır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Bu kaynak aracılığıyla kullanılabilen yazı tiplerinin listesini döndürür. |
| abstract [OpenFontDataStream](../../aspose.words.fonts/streamfontsource/openfontdatastream/)() | Bu yöntem, akışı isteğe bağlı olarak yazı tipi verileriyle açmalıdır. |

## Notlar

Akış yazı tipi kaynağını kullanmak için türetilmiş bir sınıf oluşturmalısınız.`StreamFontSource` ve uygulanmasını sağlayın[`OpenFontDataStream`](./openfontdatastream/) yöntem.

[`OpenFontDataStream`](./openfontdatastream/)yöntem birkaç kez çağrılabilir. Aspose.Words mevcut yazı tiplerinin listesini almak için sağlanan yazı tipi kaynaklarını taradığında ilk kez olarak adlandırılacak. Daha sonra, yazı tipi verilerini ayrıştırmak ve yazı tipi verilerini bazı çıktı formatlarına gömmek için belgede the yazı tipi kullanılırsa çağrılabilir.

`StreamFontSource` yazı tipi verilerinin yalnızca gerekli olduğunda yüklenmesine izin vermesi ve bunun için bellekte saklanmaması nedeniyle faydalı olabilir.[`FontSettings`](../fontsettings/) ömür.

## Örnekler

Akıştan yazı tiplerinin nasıl yükleneceğini gösterir.

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
/// Yazı tipi verilerini belleğe kaydetmek yerine yalnızca gerektiğinde yükleyin
/// "FontSettings" nesnesinin tüm ömrü boyunca.
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
* ad alanı [Aspose.Words.Fonts](../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../)
