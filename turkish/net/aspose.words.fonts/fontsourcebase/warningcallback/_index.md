---
title: FontSourceBase.WarningCallback
linktitle: WarningCallback
articleTitle: WarningCallback
second_title: .NET için Aspose.Words
description: Font kaynak işleme sırasında sorunları tespit ederek biçimlendirme doğruluğunu sağlamak için önemli olan FontSourceBase WarningCallback özelliğini keşfedin.
type: docs
weight: 30
url: /tr/net/aspose.words.fonts/fontsourcebase/warningcallback/
---
## FontSourceBase.WarningCallback property

Biçimlendirme sadakat kaybına yol açabilecek bir sorun algılandığında yazı tipi kaynağının işlenmesi sırasında çağrılır.

```csharp
public IWarningCallback WarningCallback { get; set; }
```

## Örnekler

Yazı tipi kaynaklarıyla çalışırken uyarı geri aramasının nasıl çağrılacağını gösterir.

```csharp
public void FontSourceWarning()
{
    FontSettings settings = new FontSettings();
    settings.SetFontsFolder("bad folder?", false);

    FontSourceBase source = settings.GetFontsSources()[0];
    FontSourceWarningCollector callback = new FontSourceWarningCollector();
    source.WarningCallback = callback;

    // Uyarı geri aramasını çağıracak yazı tiplerinin listesini al.
    IList<PhysicalFontInfo> fontInfos = source.GetAvailableFonts();

    Assert.True(callback.FontSubstitutionWarnings[0].Description
        .Contains("Error loading font from the folder \"bad folder?\""));
}

private class FontSourceWarningCollector : IWarningCallback
{
    /// <summary>
    /// Font kaynağının işlenmesi sırasında bir uyarı oluştuğunda her seferinde çağrılır.
    /// </summary>
    public void Warning(WarningInfo info)
    {
        FontSubstitutionWarnings.Warning(info);
    }

    public readonly WarningInfoCollection FontSubstitutionWarnings = new WarningInfoCollection();
}
```

### Ayrıca bakınız

* interface [IWarningCallback](../../../aspose.words/iwarningcallback/)
* class [FontSourceBase](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)
