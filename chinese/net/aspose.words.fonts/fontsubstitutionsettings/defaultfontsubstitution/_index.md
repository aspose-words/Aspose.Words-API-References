---
title: FontSubstitutionSettings.DefaultFontSubstitution
second_title: Aspose.Words for .NET API 参考
description: FontSubstitutionSettings 财产. 与默认字体替换规则相关的设置
type: docs
weight: 10
url: /zh/net/aspose.words.fonts/fontsubstitutionsettings/defaultfontsubstitution/
---
## FontSubstitutionSettings.DefaultFontSubstitution property

与默认字体替换规则相关的设置。

```csharp
public DefaultFontSubstitutionRule DefaultFontSubstitution { get; }
```

### 例子

演示如何设置默认字体替换规则。

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

// 将默认字体替换设置为“Courier New”。
defaultFontSubstitutionRule.DefaultFontName = "Courier New";

// 使用文档生成器，以我们不必看到替换发生的字体添加一些文本，
// 然后将结果呈现为 PDF。
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Missing Font";
builder.Writeln("Line written in a missing font, which will be substituted with Courier New.");

doc.Save(ArtifactsDir + "FontSettings.DefaultFontSubstitutionRule.pdf");
```

### 也可以看看

* class [DefaultFontSubstitutionRule](../../defaultfontsubstitutionrule/)
* class [FontSubstitutionSettings](../)
* 命名空间 [Aspose.Words.Fonts](../../fontsubstitutionsettings/)
* 部件 [Aspose.Words](../../../)


