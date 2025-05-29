---
title: LoadOptions.FontSettings
linktitle: FontSettings
articleTitle: FontSettings
second_title: Aspose.Words for .NET
description: 使用 LoadOptions FontSettings 自定义文档字体设置，提升可读性和风格。轻松优化您的文档！
type: docs
weight: 60
url: /zh/net/aspose.words.loading/loadoptions/fontsettings/
---
## LoadOptions.FontSettings property

允许指定文档字体设置。

```csharp
public FontSettings FontSettings { get; set; }
```

## 评论

加载某些格式时，Aspose.Words 可能需要解析字体。例如，加载 HTML 文档时，Aspose.Words 可能会解析字体以执行字体回退。

如果设置为`无效的`、默认静态字体设置[`DefaultInstance`](../../../aspose.words.fonts/fontsettings/defaultinstance/)将被使用。

默认值为`无效的`。

## 例子

显示如何在加载文档时应用字体替换设置。

```csharp
// 创建一个 FontSettings 对象来替换“Times New Roman”字体
// 使用来自“MyFonts”文件夹的字体“Arvo”。
FontSettings fontSettings = new FontSettings();
fontSettings.SetFontsFolder(FontsDir, false);
fontSettings.SubstitutionSettings.TableSubstitution.AddSubstitutes("Times New Roman", "Arvo");

// 将该 FontSettings 对象设置为新创建的 LoadOptions 对象的属性。
LoadOptions loadOptions = new LoadOptions();
loadOptions.FontSettings = fontSettings;

// 加载文档，然后将其呈现为带有字体替换的 PDF。
Document doc = new Document(MyDir + "Document.docx", loadOptions);

doc.Save(ArtifactsDir + "LoadOptions.FontSettings.pdf");
```

展示如何在加载期间指定字体替代。

```csharp
LoadOptions loadOptions = new LoadOptions();
loadOptions.FontSettings = new FontSettings();

// 为 LoadOptions 对象设置字体替换规则。
// 如果我们正在加载的文档使用了我们没有的字体，
// 此规则将用存在的字体替换不可用的字体。
// 在这种情况下，所有使用“MissingFont”的字体都将转换为“Comic Sans MS”。
TableSubstitutionRule substitutionRule = loadOptions.FontSettings.SubstitutionSettings.TableSubstitution;
substitutionRule.AddSubstitutes("MissingFont", "Comic Sans MS");

Document doc = new Document(MyDir + "Missing font.html", loadOptions);

// 此时此类文本仍将处于“MissingFont”状态。
// 当我们呈现文档时将发生字体替换。
Assert.AreEqual("MissingFont", doc.FirstSection.Body.FirstParagraph.Runs[0].Font.Name);

doc.Save(ArtifactsDir + "FontSettings.ResolveFontsBeforeLoadingDocument.pdf");
```

### 也可以看看

* class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* class [LoadOptions](../)
* 命名空间 [Aspose.Words.Loading](../../../aspose.words.loading/)
* 部件 [Aspose.Words](../../../)
