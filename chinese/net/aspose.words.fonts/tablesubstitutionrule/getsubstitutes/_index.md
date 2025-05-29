---
title: TableSubstitutionRule.GetSubstitutes
linktitle: GetSubstitutes
articleTitle: GetSubstitutes
second_title: Aspose.Words for .NET
description: 探索 TableSubstitutionRule 中的 GetSubstitutes 方法。轻松获取原始字体的替换字体名称，增强设计灵活性。
type: docs
weight: 20
url: /zh/net/aspose.words.fonts/tablesubstitutionrule/getsubstitutes/
---
## TableSubstitutionRule.GetSubstitutes method

返回包含指定原始字体名称的替代字体名称的数组。

```csharp
public IEnumerable<string> GetSubstitutes(string originalFontName)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| originalFontName | String | 原始字体名称。 |

### 返回值

备选字体名称列表。

## 例子

展示如何访问文档的系统字体源并设置字体替代。

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

// 将 Windows 字体目录中存在的字体设置为不存在的字体的替代字体。
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

// 重置字体源仍然会给我们留下系统字体源以及替代品。
doc.FontSettings.ResetFontSources();

Assert.AreEqual(1, doc.FontSettings.GetFontsSources().Length);
Assert.AreEqual(FontSourceType.SystemFonts, doc.FontSettings.GetFontsSources()[0].Type);
Assert.AreEqual(1,
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").Count());
Assert.True(doc.FontSettings.SubstitutionSettings.FontNameSubstitution.Enabled);
```

展示如何使用自定义字体替换表。

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// 创建一个新的表替换规则并加载默认的 Windows 字体替换表。
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;

// 如果我们只从我们的文件夹中选择字体，我们将需要一个自定义替换表。
// 我们将不再有权访问 Microsoft Windows 字体，
// 例如“Arial”或“Times New Roman”，因为它们不存在于我们的新字体文件夹中。
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
fontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

// 以下是从本地文件系统中的文件加载替换表的两种方法。
// 1 - 来自流：
using (FileStream fileStream = new FileStream(MyDir + "Font substitution rules.xml", FileMode.Open))
{
    tableSubstitutionRule.Load(fileStream);
}

// 2 - 直接从文件获取：
tableSubstitutionRule.Load(MyDir + "Font substitution rules.xml");

// 由于我们不再有权访问“Arial”，我们的字体表将首先尝试用“不存在的字体”替换它。
// 我们没有这种字体，因此它将转移到“MyFonts”文件夹中的下一个替代字体“Kreon”。
Assert.AreEqual(new[] {"Missing Font", "Kreon"}, tableSubstitutionRule.GetSubstitutes("Arial").ToArray());

// 我们可以通过编程方式扩展此表。我们将添加一个条目，将“Times New Roman”替换为“Arvo”
Assert.Null(tableSubstitutionRule.GetSubstitutes("Times New Roman"));
tableSubstitutionRule.AddSubstitutes("Times New Roman", "Arvo");
Assert.AreEqual(new[] {"Arvo"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// 我们可以使用 AddSubstitutes() 为现有字体条目添加辅助后备替代。
// 如果“Arvo”不可用，我们的表将寻找“M+ 2m”作为第二个替代选项。
tableSubstitutionRule.AddSubstitutes("Times New Roman", "M+ 2m");
Assert.AreEqual(new[] {"Arvo", "M+ 2m"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// SetSubstitutes() 可以为字体设置新的替代字体列表。
tableSubstitutionRule.SetSubstitutes("Times New Roman", "Squarish Sans CT", "M+ 2m");
Assert.AreEqual(new[] {"Squarish Sans CT", "M+ 2m"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// 使用我们无法访问的字体编写文本将调用我们的替换规则。
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Arial";
builder.Writeln("Text written in Arial, to be substituted by Kreon.");

builder.Font.Name = "Times New Roman";
builder.Writeln("Text written in Times New Roman, to be substituted by Squarish Sans CT.");

doc.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Custom.pdf");
```

### 也可以看看

* class [TableSubstitutionRule](../)
* 命名空间 [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../../)
