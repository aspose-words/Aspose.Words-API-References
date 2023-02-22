---
title: Class StreamFontSource
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Fonts.StreamFontSource sınıf. Kullanıcı tanımlı akış yazı tipi kaynağı için temel sınıf.
type: docs
weight: 2860
url: /tr/net/aspose.words.fonts/streamfontsource/
---
## StreamFontSource class

Kullanıcı tanımlı akış yazı tipi kaynağı için temel sınıf.

```csharp
public abstract class StreamFontSource : FontSourceBase
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CacheKey](../../aspose.words.fonts/streamfontsource/cachekey/) { get; } | Önbellekteki bu kaynağın anahtarı. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Yazı tipi kaynağı önceliğini döndürür. |
| [Type](../../aspose.words.fonts/streamfontsource/type/) { get; } | Yazı tipi kaynağının türünü döndürür. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Biçimlendirme aslına uygunluk kaybına neden olabilecek bir sorun algılandığında yazı tipi kaynağının işlenmesi sırasında çağrılır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Bu kaynak aracılığıyla kullanılabilen yazı tiplerinin listesini döndürür. |
| abstract [OpenFontDataStream](../../aspose.words.fonts/streamfontsource/openfontdatastream/)() | Bu yöntem, isteğe bağlı olarak yazı tipi verileriyle akışı açmalıdır. |

### Notlar

Akış yazı tipi kaynağını kullanmak için, aşağıdakilerden türetilmiş bir sınıf oluşturmalısınız.`StreamFontSource` ve aşağıdakilerin uygulanmasını sağlayın:[`OpenFontDataStream`](./openfontdatastream/) yöntem.

[`OpenFontDataStream`](./openfontdatastream/)yöntem birkaç kez çağrılabilir. Aspose.Words mevcut yazı tiplerinin listesini almak için sağlanan yazı tipi kaynaklarını taradığında ilk kez olarak adlandırılacaktır. Belgede font verilerini ayrıştırmak ve font verilerini bazı çıktı biçimlerine gömmek için the fontu kullanılıyorsa daha sonra çağrılabilir.

`StreamFontSource` yazı tipi verilerinin yalnızca gerekli olduğunda yüklenmesine izin verdiği için yararlı olabilir [`FontSettings`](../fontsettings/) ömür.

### Örnekler

Akıştan yazı tiplerinin nasıl yükleneceğini gösterir.

```csharp
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
/// Yazı tipi verilerini bellekte saklamak yerine yalnızca gerektiğinde yükleyin
/// "FontSettings" nesnesinin tüm kullanım ömrü boyunca.
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


