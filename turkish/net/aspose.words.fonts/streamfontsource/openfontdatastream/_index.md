---
title: StreamFontSource.OpenFontDataStream
second_title: Aspose.Words for .NET API Referansı
description: StreamFontSource yöntem. Bu yöntem akışı isteğe bağlı olarak yazı tipi verileriyle açmalıdır.
type: docs
weight: 30
url: /tr/net/aspose.words.fonts/streamfontsource/openfontdatastream/
---
## StreamFontSource.OpenFontDataStream method

Bu yöntem, akışı isteğe bağlı olarak yazı tipi verileriyle açmalıdır.

```csharp
public abstract Stream OpenFontDataStream()
```

### Geri dönüş değeri

Yazı tipi veri akışı.

### Notlar

Yayın okunduktan sonra kapatılacak. Açıkça kapatmanıza gerek yoktur.

### Örnekler

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

* class [StreamFontSource](../)
* ad alanı [Aspose.Words.Fonts](../../streamfontsource/)
* toplantı [Aspose.Words](../../../)


