---
title: SystemFontSource Class
linktitle: SystemFontSource
articleTitle: SystemFontSource
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Fonts.SystemFontSource 班级. 表示系统中安装的所有 TrueType 字体 在 C#.
type: docs
weight: 3050
url: /zh/net/aspose.words.fonts/systemfontsource/
---
## SystemFontSource class

表示系统中安装的所有 TrueType 字体。

要了解更多信息，请访问[使用字体](https://docs.aspose.com/words/net/working-with-fonts/)文档文章。

```csharp
public class SystemFontSource : FontSourceBase
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [SystemFontSource](systemfontsource/#constructor)() | 向量. |
| [SystemFontSource](systemfontsource/#constructor_1)(*int*) | 向量. |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | 返回字体源优先级。 |
| override [Type](../../aspose.words.fonts/systemfontsource/type/) { get; } | 返回字体源的类型。 |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | 在处理字体源期间检测到可能导致格式保真度损失的问题时调用。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | 返回通过此源可用的字体列表。 |
| static [GetSystemFontFolders](../../aspose.words.fonts/systemfontsource/getsystemfontfolders/)() | 返回系统字体文件夹或空数组（如果文件夹不可访问）。 |

## 例子

演示如何访问文档的系统字体源并设置字体替代品。

```csharp
Document doc = new Document();
doc.FontSettings = new FontSettings();

// 默认情况下，空白文档始终包含系统字体源。
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

// 设置 Windows Fonts 目录中存在的字体来替代不存在的字体。
doc.FontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;
doc.FontSettings.SubstitutionSettings.TableSubstitution.AddSubstitutes("Kreon-Regular", new[] {"Calibri"});

Assert.AreEqual(1,
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").Count());
Assert.Contains("Calibri",
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").ToArray());

// 或者，我们可以添加一个文件夹字体源，其中相应的文件夹包含字体。
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
doc.FontSettings.SetFontsSources(new FontSourceBase[] {systemFontSource, folderFontSource});
Assert.AreEqual(2, doc.FontSettings.GetFontsSources().Length);

// 重置字体源仍然让我们保留系统字体源以及替代品。
doc.FontSettings.ResetFontSources();

Assert.AreEqual(1, doc.FontSettings.GetFontsSources().Length);
Assert.AreEqual(FontSourceType.SystemFonts, doc.FontSettings.GetFontsSources()[0].Type);
Assert.AreEqual(1,
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").Count());
```

### 也可以看看

* class [FontSourceBase](../fontsourcebase/)
* 命名空间 [Aspose.Words.Fonts](../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../)
