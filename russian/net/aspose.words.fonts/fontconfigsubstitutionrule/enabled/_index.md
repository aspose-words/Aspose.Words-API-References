---
title: FontConfigSubstitutionRule.Enabled
linktitle: Enabled
articleTitle: Enabled
second_title: Aspose.Words для .NET
description: Узнайте, как управлять свойством FontConfigSubstitutionRule Enabled, чтобы оптимизировать настройки шрифтов и повысить гибкость дизайна.
type: docs
weight: 10
url: /ru/net/aspose.words.fonts/fontconfigsubstitutionrule/enabled/
---
## FontConfigSubstitutionRule.Enabled property

Указывает, включено правило или нет.

```csharp
public override bool Enabled { set; }
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
