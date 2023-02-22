---
title: FontSubstitutionRule.Enabled
second_title: Справочник по API Aspose.Words для .NET
description: FontSubstitutionRule свойство. Указывает включено ли правило.
type: docs
weight: 10
url: /ru/net/aspose.words.fonts/fontsubstitutionrule/enabled/
---
## FontSubstitutionRule.Enabled property

Указывает, включено ли правило.

```csharp
public virtual bool Enabled { get; set; }
```

### Примеры

Показывает подстановку конфигурации шрифта в зависимости от операционной системы.

```csharp
FontSettings fontSettings = new FontSettings();
FontConfigSubstitutionRule fontConfigSubstitution =
    fontSettings.SubstitutionSettings.FontConfigSubstitution;

bool isWindows = new[] {PlatformID.Win32NT, PlatformID.Win32S, PlatformID.Win32Windows, PlatformID.WinCE}
    .Any(p => Environment.OSVersion.Platform == p);

// Объект FontConfigSubstitutionRule работает по-разному на платформах Windows/отличных от Windows.
// В Windows он недоступен.
if (isWindows)
{
    Assert.False(fontConfigSubstitution.Enabled);
    Assert.False(fontConfigSubstitution.IsFontConfigAvailable());
}

bool isLinuxOrMac =
    new[] {PlatformID.Unix, PlatformID.MacOSX}.Any(p => Environment.OSVersion.Platform == p);

// В Linux/Mac у нас будет к нему доступ, и мы сможем выполнять операции.
if (isLinuxOrMac)
{
    Assert.True(fontConfigSubstitution.Enabled);
    Assert.True(fontConfigSubstitution.IsFontConfigAvailable());

    fontConfigSubstitution.ResetCache();
}
```

Показывает, как получить доступ к источнику системного шрифта документа и установить заменители шрифта.

```csharp
Document doc = new Document();
doc.FontSettings = new FontSettings();

// По умолчанию пустой документ всегда содержит системный источник шрифта.
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

// Установите шрифт, существующий в каталоге шрифтов Windows, в качестве замены несуществующего.
doc.FontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;
doc.FontSettings.SubstitutionSettings.TableSubstitution.AddSubstitutes("Kreon-Regular", new[] {"Calibri"});

Assert.AreEqual(1,
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").Count());
Assert.Contains("Calibri",
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").ToArray());

// В качестве альтернативы мы могли бы добавить папку источника шрифта, в которой соответствующая папка содержит шрифт.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
doc.FontSettings.SetFontsSources(new FontSourceBase[] {systemFontSource, folderFontSource});
Assert.AreEqual(2, doc.FontSettings.GetFontsSources().Length);

// Сброс источников шрифта по-прежнему оставляет нам источник системного шрифта, а также наши заменители.
doc.FontSettings.ResetFontSources();

Assert.AreEqual(1, doc.FontSettings.GetFontsSources().Length);
Assert.AreEqual(FontSourceType.SystemFonts, doc.FontSettings.GetFontsSources()[0].Type);
Assert.AreEqual(1,
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").Count());
```

### Смотрите также

* class [FontSubstitutionRule](../)
* пространство имен [Aspose.Words.Fonts](../../fontsubstitutionrule/)
* сборка [Aspose.Words](../../../)


