---
title: FontConfigSubstitutionRule.IsFontConfigAvailable
linktitle: IsFontConfigAvailable
articleTitle: IsFontConfigAvailable
second_title: .NET için Aspose.Words
description: FontConfig yardımcı programının IsFontConfigAvailable yöntemiyle kullanılabilir olup olmadığını keşfedin. Uygulamalarınız için optimum font yönetimini sağlayın.
type: docs
weight: 20
url: /tr/net/aspose.words.fonts/fontconfigsubstitutionrule/isfontconfigavailable/
---
## FontConfigSubstitutionRule.IsFontConfigAvailable method

Fontconfig yardımcı programının kullanılabilir olup olmadığını kontrol edin.

```csharp
public bool IsFontConfigAvailable()
```

## Örnekler

İşletim sistemine bağlı font yapılandırması değişimini gösterir.

```csharp
FontSettings fontSettings = new FontSettings();
FontConfigSubstitutionRule fontConfigSubstitution =
    fontSettings.SubstitutionSettings.FontConfigSubstitution;

bool isWindows = new[] {PlatformID.Win32NT, PlatformID.Win32S, PlatformID.Win32Windows, PlatformID.WinCE}
    .Any(p => Environment.OSVersion.Platform == p);

// FontConfigSubstitutionRule nesnesi Windows/Windows olmayan platformlarda farklı çalışır.
// Windows'ta kullanılamaz.
if (isWindows)
{
    Assert.False(fontConfigSubstitution.Enabled);
    Assert.False(fontConfigSubstitution.IsFontConfigAvailable());
}

bool isLinuxOrMac =
    new[] {PlatformID.Unix, PlatformID.MacOSX}.Any(p => Environment.OSVersion.Platform == p);

// Linux/Mac'te buna erişebileceğiz ve işlemler yapabileceğiz.
if (isLinuxOrMac)
{
    Assert.True(fontConfigSubstitution.Enabled);
    Assert.True(fontConfigSubstitution.IsFontConfigAvailable());

    fontConfigSubstitution.ResetCache();
}
```

### Ayrıca bakınız

* class [FontConfigSubstitutionRule](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)
