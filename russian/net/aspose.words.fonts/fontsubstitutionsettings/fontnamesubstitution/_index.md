---
title: FontSubstitutionSettings.FontNameSubstitution
linktitle: FontNameSubstitution
articleTitle: FontNameSubstitution
second_title: Aspose.Words для .NET
description: Оптимизируйте типографику с помощью FontSubstitutionSettings. Узнайте, как настроить правила именования шрифтов для повышения гибкости дизайна и удобства для пользователя.
type: docs
weight: 40
url: /ru/net/aspose.words.fonts/fontsubstitutionsettings/fontnamesubstitution/
---
## FontSubstitutionSettings.FontNameSubstitution property

Настройки, связанные с правилом подстановки имени шрифта.

```csharp
public FontNameSubstitutionRule FontNameSubstitution { get; }
```

## Примеры

Показывает, как получить доступ к системному источнику шрифтов документа и задать замену шрифтов.

```csharp
Document doc = new Document();
doc.FontSettings = new FontSettings();

// По умолчанию пустой документ всегда содержит источник системного шрифта.
Assert.AreEqual(1, doc.FontSettings.GetFontsSources().Length);

SystemFontSource systemFontSource = (SystemFontSource) doc.FontSettings.GetFontsSources()[0];
Assert.AreEqual(FontSourceType.SystemFonts, systemFontSource.Type);
Assert.AreEqual(0, systemFontSource.Priority);

PlatformID pid = Environment.OSVersion.Platform;
bool isWindows = (pid == PlatformID.Win32NT) || (pid == PlatformID.Win32S) ||
                 (pid == PlatformID.Win32Windows) || (pid == PlatformID.WinCE);
if (isWindows)
{
    const string fontsPath = @"C:\WINDOWS\Fonts";
    Assert.AreEqual(fontsPath.ToLower(),
        SystemFontSource.GetSystemFontFolders().FirstOrDefault()?.ToLower());
}

foreach (string systemFontFolder in SystemFontSource.GetSystemFontFolders())
{
    Console.WriteLine(systemFontFolder);
}

// Установить шрифт, который существует в каталоге шрифтов Windows, в качестве замены отсутствующему.
doc.FontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;
doc.FontSettings.SubstitutionSettings.TableSubstitution.AddSubstitutes("Kreon-Regular", new[] {"Calibri"});

Assert.AreEqual(1,
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").Count());
Assert.Contains("Calibri",
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").ToArray());

// В качестве альтернативы мы могли бы добавить папку-источник шрифта, в которой соответствующая папка содержит шрифт.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
doc.FontSettings.SetFontsSources(new FontSourceBase[] {systemFontSource, folderFontSource});
Assert.AreEqual(2, doc.FontSettings.GetFontsSources().Length);

// Сброс источников шрифтов по-прежнему оставляет нам системный источник шрифтов, а также наши заменители.
doc.FontSettings.ResetFontSources();

Assert.AreEqual(1, doc.FontSettings.GetFontsSources().Length);
Assert.AreEqual(FontSourceType.SystemFonts, doc.FontSettings.GetFontsSources()[0].Type);
Assert.AreEqual(1,
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").Count());
Assert.True(doc.FontSettings.SubstitutionSettings.FontNameSubstitution.Enabled);
```

### Смотрите также

* class [FontNameSubstitutionRule](../../fontnamesubstitutionrule/)
* class [FontSubstitutionSettings](../)
* пространство имен [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* сборка [Aspose.Words](../../../)
