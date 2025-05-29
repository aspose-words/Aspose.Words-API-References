---
title: DefaultFontSubstitutionRule Class
linktitle: DefaultFontSubstitutionRule
articleTitle: DefaultFontSubstitutionRule
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Fonts.DefaultFontSubstitutionRule 类，实现无缝字体管理和增强的文档格式。立即优化您的工作流程！
type: docs
weight: 3250
url: /zh/net/aspose.words.fonts/defaultfontsubstitutionrule/
---
## DefaultFontSubstitutionRule class

默认字体替换规则。

要了解更多信息，请访问[使用字体](https://docs.aspose.com/words/net/working-with-fonts/)文档文章。

```csharp
public class DefaultFontSubstitutionRule : FontSubstitutionRule
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [DefaultFontName](../../aspose.words.fonts/defaultfontsubstitutionrule/defaultfontname/) { get; set; } | 获取或设置默认字体名称。 |
| virtual [Enabled](../../aspose.words.fonts/fontsubstitutionrule/enabled/) { get; set; } | 指定规则是否启用。 |

## 评论

如果原始字体不可用，此规则将定义用于替换的单个默认字体名称。

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

### 也可以看看

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* 命名空间 [Aspose.Words.Fonts](../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../)
