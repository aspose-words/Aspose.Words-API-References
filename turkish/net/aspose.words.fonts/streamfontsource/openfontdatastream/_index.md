---
title: StreamFontSource.OpenFontDataStream
linktitle: OpenFontDataStream
articleTitle: OpenFontDataStream
second_title: .NET için Aspose.Words
description: İsteğe bağlı olarak yazı tipi veri akışlarına verimli bir şekilde erişmek ve tasarım iş akışınızı geliştirmek için StreamFontSource OpenFontDataStream yöntemini keşfedin.
type: docs
weight: 30
url: /tr/net/aspose.words.fonts/streamfontsource/openfontdatastream/
---
## StreamFontSource.OpenFontDataStream method

Bu yöntem, akışı talep üzerine yazı tipi verileriyle açmalıdır.

```csharp
public abstract Stream OpenFontDataStream()
```

### Geri dönüş değeri

Yazı tipi veri akışı.

## Notlar

Akış okunduktan sonra kapatılacak. Açıkça kapatılmasına gerek yok.

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

* class [StreamFontSource](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)
