---
title: FontConfigSubstitutionRule.ResetCache
second_title: Aspose.Words for .NET API Referansı
description: FontConfigSubstitutionRule yöntem. fontconfig arama sonuçlarının önbelleğini sıfırlar.
type: docs
weight: 30
url: /tr/net/aspose.words.fonts/fontconfigsubstitutionrule/resetcache/
---
## FontConfigSubstitutionRule.ResetCache method

fontconfig arama sonuçlarının önbelleğini sıfırlar.

```csharp
public void ResetCache()
```

### Örnekler

İşletim sistemine bağlı yazı tipi yapılandırma değişikliğini gösterir.

```csharp
FontSettings fontSettings = new FontSettings();
FontConfigSubstitutionRule fontConfigSubstitution =
    fontSettings.SubstitutionSettings.FontConfigSubstitution;

bool isWindows = new[] {PlatformID.Win32NT, PlatformID.Win32S, PlatformID.Win32Windows, PlatformID.WinCE}
    .Any(p => Environment.OSVersion.Platform == p);

// FontConfigSubstitutionRule nesnesi, Windows/Windows olmayan platformlarda farklı çalışır.
// Windows'ta kullanılamaz.
if (isWindows)
{
    Assert.False(fontConfigSubstitution.Enabled);
    Assert.False(fontConfigSubstitution.IsFontConfigAvailable());
}

bool isLinuxOrMac =
    new[] {PlatformID.Unix, PlatformID.MacOSX}.Any(p => Environment.OSVersion.Platform == p);

// Linux/Mac'te ona erişimimiz olacak ve işlemler yapabileceğiz.
if (isLinuxOrMac)
{
    Assert.True(fontConfigSubstitution.Enabled);
    Assert.True(fontConfigSubstitution.IsFontConfigAvailable());

    fontConfigSubstitution.ResetCache();
}
```

### Ayrıca bakınız

* class [FontConfigSubstitutionRule](../)
* ad alanı [Aspose.Words.Fonts](../../fontconfigsubstitutionrule/)
* toplantı [Aspose.Words](../../../)


