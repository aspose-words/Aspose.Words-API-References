---
title: TableSubstitutionRule.SetSubstitutes
second_title: Aspose.Words for .NET API 参考
description: TableSubstitutionRule 方法. 覆盖给定原始字体名称的替代字体名称
type: docs
weight: 80
url: /zh/net/aspose.words.fonts/tablesubstitutionrule/setsubstitutes/
---
## TableSubstitutionRule.SetSubstitutes method

覆盖给定原始字体名称的替代字体名称。

```csharp
public void SetSubstitutes(string originalFontName, params string[] substituteFontNames)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| originalFontName | String | 原始字体名称。 |
| substituteFontNames | String[] | 替代字体名称列表。 |

### 例子

显示如何设置字体替换规则。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();

// 默认字体源包含文档使用的第一个字体。
Assert.AreEqual(1, fontSources.Length);
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// 第二种字体“Amethysta”不可用。
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// 我们可以配置一个字体替换表来确定
// Aspose.Words 将使用哪些字体来替代不可用的字体。
// 为“Amethysta”设置两种替换字体：“Arvo”和“Courier New”。
// 如果第一个替代品不可用，Aspose.Words 会尝试使用第二个替代品，依此类推。
doc.FontSettings = new FontSettings();
doc.FontSettings.SubstitutionSettings.TableSubstitution.SetSubstitutes(
    "Amethysta", new[] {"Arvo", "Courier New"});

 // “Amethysta”不可用，并且替换规则规定第一个用作替换的字体是“Arvo”。
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

 // “Arvo”也不可用，但“Courier New”可用。
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Courier New"));

// 输出文档将显示使用“Amethysta”字体、格式为“Courier New”的文本。
doc.Save(ArtifactsDir + "FontSettings.TableSubstitution.pdf");
```

展示如何使用自定义字体替换表。

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// 创建新的表替换规则并加载默认的 Windows 字体替换表。
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;

// 如果我们只从文件夹中选择字体，我们将需要一个自定义替换表。
// 我们将无法再访问 Microsoft Windows 字体，
// 例如“Arial”或“Times New Roman”，因为它们不存在于我们的新字体文件夹中。
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
fontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

// 下面是从本地文件系统中的文件加载替换表的两种方法。
// 1 - 来自流：
using (FileStream fileStream = new FileStream(MyDir + "Font substitution rules.xml", FileMode.Open))
{
    tableSubstitutionRule.Load(fileStream);
}

// 2 - 直接来自文件：
tableSubstitutionRule.Load(MyDir + "Font substitution rules.xml");

// 由于我们不再有权访问“Arial”，我们的字体表将首先尝试用“不存在的字体”替换它。
// 我们没有此字体，因此它将移至“MyFonts”文件夹中找到的下一个替代字体“Kreon”。
Assert.AreEqual(new[] {"Missing Font", "Kreon"}, tableSubstitutionRule.GetSubstitutes("Arial").ToArray());

// 我们可以通过编程方式扩展该表。我们将添加一个条目，将“Times New Roman”替换为“Arvo”
Assert.Null(tableSubstitutionRule.GetSubstitutes("Times New Roman"));
tableSubstitutionRule.AddSubstitutes("Times New Roman", "Arvo");
Assert.AreEqual(new[] {"Arvo"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// 我们可以使用 AddSubstitutes() 添加现有字体条目的辅助后备替代。
// 如果“Arvo”不可用，我们的表将寻找“M+ 2m”作为第二个替代选项。
tableSubstitutionRule.AddSubstitutes("Times New Roman", "M+ 2m");
Assert.AreEqual(new[] {"Arvo", "M+ 2m"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// SetSubstitutes() 可以为某种字体设置新的替代字体列表。
tableSubstitutionRule.SetSubstitutes("Times New Roman", new[] {"Squarish Sans CT", "M+ 2m"});
Assert.AreEqual(new[] {"Squarish Sans CT", "M+ 2m"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// 使用我们无权访问的字体编写文本将调用我们的替换规则。
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Arial";
builder.Writeln("Text written in Arial, to be substituted by Kreon.");

builder.Font.Name = "Times New Roman";
builder.Writeln("Text written in Times New Roman, to be substituted by Squarish Sans CT.");

doc.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Custom.pdf");
```

### 也可以看看

* class [TableSubstitutionRule](../)
* 命名空间 [Aspose.Words.Fonts](../../tablesubstitutionrule/)
* 部件 [Aspose.Words](../../../)


