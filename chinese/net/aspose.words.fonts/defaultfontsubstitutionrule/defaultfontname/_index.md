---
title: DefaultFontSubstitutionRule.DefaultFontName
linktitle: DefaultFontName
articleTitle: DefaultFontName
second_title: Aspose.Words for .NET
description: 了解如何轻松管理 DefaultFontSubstitutionRule 并自定义默认字体名称以增强设计灵活性。
type: docs
weight: 10
url: /zh/net/aspose.words.fonts/defaultfontsubstitutionrule/defaultfontname/
---
## DefaultFontSubstitutionRule.DefaultFontName property

获取或设置默认字体名称。

```csharp
public string DefaultFontName { get; set; }
```

## 评论

默认值为“Times New Roman”。

## 例子

显示如何设置默认字体替换规则。

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// 获取 FontSettings 中的默认替换规则。
// 此规则将用“Times New Roman”替换所有缺失的字体。
DefaultFontSubstitutionRule defaultFontSubstitutionRule =
    fontSettings.SubstitutionSettings.DefaultFontSubstitution;
Assert.True(defaultFontSubstitutionRule.Enabled);
Assert.AreEqual("Times New Roman", defaultFontSubstitutionRule.DefaultFontName);

// 将默认字体替代设置为“Courier New”。
defaultFontSubstitutionRule.DefaultFontName = "Courier New";

// 使用文档生成器，添加一些我们不需要看到替换发生的字体的文本，
// 然后将结果呈现为 PDF。
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Missing Font";
builder.Writeln("Line written in a missing font, which will be substituted with Courier New.");

doc.Save(ArtifactsDir + "FontSettings.DefaultFontSubstitutionRule.pdf");
```

显示如何指定默认字体。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Arvo";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();

// 文档使用的字体源包含字体“Arial”，但不包含字体“Arvo”。
Assert.AreEqual(1, fontSources.Length);
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// 将“DefaultFontName”属性设置为“Courier New”，
// 在呈现文档时，当其他字体不可用时，在所有情况下都应用该字体。
FontSettings.DefaultInstance.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Courier New";

Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Courier New"));

// Aspose.Words 现在将在任何渲染调用期间使用默认字体代替任何缺失的字体。
doc.Save(ArtifactsDir + "FontSettings.DefaultFontName.pdf");
```

### 也可以看看

* class [DefaultFontSubstitutionRule](../)
* 命名空间 [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../../)
