---
title: FontConfigSubstitutionRule Class
linktitle: FontConfigSubstitutionRule
articleTitle: FontConfigSubstitutionRule
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Fonts.FontConfigSubstitutionRule для бесшовного управления шрифтами и настройки в ваших документах. Улучшите свой стиль текста сегодня!
type: docs
weight: 3300
url: /ru/net/aspose.words.fonts/fontconfigsubstitutionrule/
---
## FontConfigSubstitutionRule class

Правило подстановки конфигурации шрифта.

Чтобы узнать больше, посетите[Работа со шрифтами](https://docs.aspose.com/words/net/working-with-fonts/) документальная статья.

```csharp
public class FontConfigSubstitutionRule : FontSubstitutionRule
```

## Характеристики

| Имя | Описание |
| --- | --- |
| override [Enabled](../../aspose.words.fonts/fontconfigsubstitutionrule/enabled/) { set; } | Указывает, включено правило или нет. |

## Методы

| Имя | Описание |
| --- | --- |
| [IsFontConfigAvailable](../../aspose.words.fonts/fontconfigsubstitutionrule/isfontconfigavailable/)() | Проверьте, доступна ли утилита fontconfig. |
| [ResetCache](../../aspose.words.fonts/fontconfigsubstitutionrule/resetcache/)() | Сбрасывает кэш результатов вызова fontconfig. |

## Примечания

Это правило использует утилиту fontconfig на Linux (и других Unix-подобных) платформах для получения подстановки , если исходный шрифт недоступен.

Если утилита fontconfig недоступна, то это правило будет проигнорировано.

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

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* пространство имен [Aspose.Words.Fonts](../../aspose.words.fonts/)
* сборка [Aspose.Words](../../)
