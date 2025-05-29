---
title: HtmlFixedSaveOptions.UseTargetMachineFonts
linktitle: UseTargetMachineFonts
articleTitle: UseTargetMachineFonts
second_title: Aspose.Words for .NET
description: 了解 HtmlFixedSaveOptions 中的 UseTargetMachineFonts 属性如何利用目标机器字体增强文档显示效果。立即优化您的字体管理！
type: docs
weight: 210
url: /zh/net/aspose.words.saving/htmlfixedsaveoptions/usetargetmachinefonts/
---
## HtmlFixedSaveOptions.UseTargetMachineFonts property

标志指示是否必须使用目标机器的字体来显示文档。 如果将此标志设置为`真的`，[`FontFormat`](../fontformat/)和[`ExportEmbeddedFonts`](../exportembeddedfonts/)属性不起作用， 也不起作用[`ResourceSavingCallback`](../resourcesavingcallback/)不会因字体而触发。 默认为`错误的`.

```csharp
public bool UseTargetMachineFonts { get; set; }
```

## 例子

展示如何将文档保存为 HTML 时仅使用目标机器的字体。

```csharp
Document doc = new Document(MyDir + "Bullet points with alternative font.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedCss = true,
    UseTargetMachineFonts = useTargetMachineFonts,
    FontFormat = ExportFontFormat.Ttf,
    ExportEmbeddedFonts = false,
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.UsingMachineFonts.html");

if (useTargetMachineFonts)
    Assert.False(Regex.Match(outDocContents, "@font-face").Success);
else
    Assert.True(Regex.Match(outDocContents,
        "@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], " +
        "url[(]'HtmlFixedSaveOptions.UsingMachineFonts/font001.ttf'[)] format[(]'truetype'[)]; }").Success);
```

### 也可以看看

* class [HtmlFixedSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
