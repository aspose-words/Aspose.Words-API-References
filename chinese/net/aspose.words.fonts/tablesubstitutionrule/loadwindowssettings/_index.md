---
title: TableSubstitutionRule.LoadWindowsSettings
linktitle: LoadWindowsSettings
articleTitle: LoadWindowsSettings
second_title: Aspose.Words for .NET
description: 使用 LoadWindowsSettings 方法轻松加载 Windows 预定义的表替换设置。立即优化您的工作流程！
type: docs
weight: 60
url: /zh/net/aspose.words.fonts/tablesubstitutionrule/loadwindowssettings/
---
## TableSubstitutionRule.LoadWindowsSettings method

加载适用于 Windows 平台的预定义表替换设置。

```csharp
public void LoadWindowsSettings()
```

## 例子

展示如何访问 Windows 和 Linux 的字体替换表。

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// 创建一个新的表替换规则并加载默认的 Microsoft Windows 字体替换表。
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;
tableSubstitutionRule.LoadWindowsSettings();

// 在 Windows 中，“Times New Roman CE”字体的默认替代字体是“Times New Roman”。
Assert.AreEqual(new[] {"Times New Roman"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// 我们可以将表保存为 XML 文档的形式。
tableSubstitutionRule.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Windows.xml");

// Linux 有自己的替换表。
// “Times New Roman CE” 有多个替代字体。
// 如果第一个替代品“FreeSerif”也不可用，
// 此规则将循环遍历数组中的其他规则，直到找到可用的规则。
tableSubstitutionRule.LoadLinuxSettings();
Assert.AreEqual(new[] {"FreeSerif", "Liberation Serif", "DejaVu Serif"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// 使用流将 Linux 替换表保存为 XML 文档的形式。
using (FileStream fileStream = new FileStream(ArtifactsDir + "FontSettings.TableSubstitutionRule.Linux.xml",
    FileMode.Create))
{
    tableSubstitutionRule.Save(fileStream);
}
```

### 也可以看看

* class [TableSubstitutionRule](../)
* 命名空间 [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../../)
