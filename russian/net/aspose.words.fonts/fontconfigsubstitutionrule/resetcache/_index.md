---
title: FontConfigSubstitutionRule.ResetCache
linktitle: ResetCache
articleTitle: ResetCache
second_title: Aspose.Words для .NET
description: Оптимизируйте управление шрифтами с помощью метода FontConfigSubstitutionRule ResetCache. Легко очищайте результаты fontconfig для повышения производительности.
type: docs
weight: 30
url: /ru/net/aspose.words.fonts/fontconfigsubstitutionrule/resetcache/
---
## FontConfigSubstitutionRule.ResetCache method

Сбрасывает кэш результатов вызова fontconfig.

```csharp
public void ResetCache()
```

## Примеры

Показывает замену конфигурации шрифтов, зависящую от операционной системы.

```csharp
FontSettings fontSettings = new FontSettings();
FontConfigSubstitutionRule fontConfigSubstitution =
    fontSettings.SubstitutionSettings.FontConfigSubstitution;

bool isWindows = new[] {PlatformID.Win32NT, PlatformID.Win32S, PlatformID.Win32Windows, PlatformID.WinCE}
    .Any(p => Environment.OSVersion.Platform == p);

// Объект FontConfigSubstitutionRule работает по-разному на платформах Windows и других платформах.
// В Windows это недоступно.
if (isWindows)
{
    Assert.False(fontConfigSubstitution.Enabled);
    Assert.False(fontConfigSubstitution.IsFontConfigAvailable());
}

bool isLinuxOrMac =
    new[] {PlatformID.Unix, PlatformID.MacOSX}.Any(p => Environment.OSVersion.Platform == p);

// На Linux/Mac у нас будет к нему доступ, и мы сможем выполнять операции.
if (isLinuxOrMac)
{
    Assert.True(fontConfigSubstitution.Enabled);
    Assert.True(fontConfigSubstitution.IsFontConfigAvailable());

    fontConfigSubstitution.ResetCache();
}
```

### Смотрите также

* class [FontConfigSubstitutionRule](../)
* пространство имен [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* сборка [Aspose.Words](../../../)
