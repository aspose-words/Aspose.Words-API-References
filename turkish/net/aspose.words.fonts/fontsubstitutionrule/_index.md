---
title: FontSubstitutionRule Class
linktitle: FontSubstitutionRule
articleTitle: FontSubstitutionRule
second_title: .NET için Aspose.Words
description: Belge işleme ve tasarımında etkili font değişimi için temel kılavuzunuz olan Aspose.Words.Fonts.FontSubstitutionRule sınıfını keşfedin.
type: docs
weight: 3430
url: /tr/net/aspose.words.fonts/fontsubstitutionrule/
---
## FontSubstitutionRule class

Bu, yazı tipi değiştirme kuralı için soyut bir temel sınıftır.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Yazı Tipleriyle Çalışma](https://docs.aspose.com/words/net/working-with-fonts/) belgeleme makalesi.

```csharp
public abstract class FontSubstitutionRule
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| virtual [Enabled](../../aspose.words.fonts/fontsubstitutionrule/enabled/) { get; set; } | Kuralın etkin olup olmadığını belirtir. |

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

* ad alanı [Aspose.Words.Fonts](../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../)
