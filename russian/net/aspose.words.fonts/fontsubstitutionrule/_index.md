---
title: FontSubstitutionRule Class
linktitle: FontSubstitutionRule
articleTitle: FontSubstitutionRule
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Fonts.FontSubstitutionRule — ваше основное руководство по эффективной замене шрифтов при обработке и дизайне документов.
type: docs
weight: 3430
url: /ru/net/aspose.words.fonts/fontsubstitutionrule/
---
## FontSubstitutionRule class

Это абстрактный базовый класс для правила замены шрифта.

Чтобы узнать больше, посетите[Работа со шрифтами](https://docs.aspose.com/words/net/working-with-fonts/) документальная статья.

```csharp
public abstract class FontSubstitutionRule
```

## Характеристики

| Имя | Описание |
| --- | --- |
| virtual [Enabled](../../aspose.words.fonts/fontsubstitutionrule/enabled/) { get; set; } | Указывает, включено правило или нет. |

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

* пространство имен [Aspose.Words.Fonts](../../aspose.words.fonts/)
* сборка [Aspose.Words](../../)
