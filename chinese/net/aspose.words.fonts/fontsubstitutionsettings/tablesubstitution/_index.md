---
title: FontSubstitutionSettings.TableSubstitution
second_title: Aspose.Words for .NET API 参考
description: FontSubstitutionSettings 财产. 与表替换规则相关的设置
type: docs
weight: 50
url: /zh/net/aspose.words.fonts/fontsubstitutionsettings/tablesubstitution/
---
## FontSubstitutionSettings.TableSubstitution property

与表替换规则相关的设置。

```csharp
public TableSubstitutionRule TableSubstitution { get; }
```

### 例子

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

* class [TableSubstitutionRule](../../tablesubstitutionrule/)
* class [FontSubstitutionSettings](../)
* 命名空间 [Aspose.Words.Fonts](../../fontsubstitutionsettings/)
* 部件 [Aspose.Words](../../../)


