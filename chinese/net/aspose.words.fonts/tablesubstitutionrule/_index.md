---
title: TableSubstitutionRule Class
linktitle: TableSubstitutionRule
articleTitle: TableSubstitutionRule
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Fonts.TableSubstitutionRule 班级. 表字体替换规则 在 C#.
type: docs
weight: 3060
url: /zh/net/aspose.words.fonts/tablesubstitutionrule/
---
## TableSubstitutionRule class

表字体替换规则.

要了解更多信息，请访问[使用字体](https://docs.aspose.com/words/net/working-with-fonts/)文档文章。

```csharp
public class TableSubstitutionRule : FontSubstitutionRule
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| virtual [Enabled](../../aspose.words.fonts/fontsubstitutionrule/enabled/) { get; set; } | 指定是否启用规则。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [AddSubstitutes](../../aspose.words.fonts/tablesubstitutionrule/addsubstitutes/)(*string, params string[]*) | 添加给定原始字体名称的替代字体名称。 |
| [GetSubstitutes](../../aspose.words.fonts/tablesubstitutionrule/getsubstitutes/)(*string*) | 返回包含指定原始字体名称的替代字体名称的数组。 |
| [Load](../../aspose.words.fonts/tablesubstitutionrule/load/#load)(*Stream*) | 从 XML 流加载表替换设置。 |
| [Load](../../aspose.words.fonts/tablesubstitutionrule/load/#load_1)(*string*) | 从 XML 文件加载表替换设置。 |
| [LoadAndroidSettings](../../aspose.words.fonts/tablesubstitutionrule/loadandroidsettings/)() | 加载 Android 平台的预定义表替换设置。 |
| [LoadLinuxSettings](../../aspose.words.fonts/tablesubstitutionrule/loadlinuxsettings/)() | 加载 Linux 平台的预定义表替换设置。 |
| [LoadWindowsSettings](../../aspose.words.fonts/tablesubstitutionrule/loadwindowssettings/)() | 加载 Windows 平台的预定义表替换设置。 |
| [Save](../../aspose.words.fonts/tablesubstitutionrule/save/#save)(*Stream*) | 将当前表替换设置保存到流中。 |
| [Save](../../aspose.words.fonts/tablesubstitutionrule/save/#save_1)(*string*) | 将当前表替换设置保存到文件。 |
| [SetSubstitutes](../../aspose.words.fonts/tablesubstitutionrule/setsubstitutes/)(*string, params string[]*) | 覆盖给定原始字体名称的替代字体名称。 |

## 评论

此规则定义在原始字体不可用时要使用的替代字体名称列表。 将检查替代字体名称和字体名称[`AltName`](../fontinfo/altname/)（如果有）.

## 例子

演示如何访问 Windows 和 Linux 的字体替换表。

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// 创建新的表替换规则并加载默认的 Microsoft Windows 字体替换表。
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;
tableSubstitutionRule.LoadWindowsSettings();

// 在 Windows 中，“Times New Roman CE”字体的默认替代字体是“Times New Roman”。
Assert.AreEqual(new[] {"Times New Roman"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// 我们可以将表保存为XML文档的形式。
tableSubstitutionRule.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Windows.xml");

// Linux 有自己的替换表。
// “Times New Roman CE”有多种替代字体。
// 如果第一个替换，“FreeSerif”也不可用，
// 该规则将循环遍历数组中的其他规则，直到找到可用的规则。
tableSubstitutionRule.LoadLinuxSettings();
Assert.AreEqual(new[] {"FreeSerif", "Liberation Serif", "DejaVu Serif"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// 使用流以 XML 文档的形式保存 Linux 替换表。
using (FileStream fileStream = new FileStream(ArtifactsDir + "FontSettings.TableSubstitutionRule.Linux.xml",
    FileMode.Create))
{
    tableSubstitutionRule.Save(fileStream);
}
```

### 也可以看看

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* 命名空间 [Aspose.Words.Fonts](../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../)
