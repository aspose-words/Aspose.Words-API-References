---
title: ExportFontFormat Enum
linktitle: ExportFontFormat
articleTitle: ExportFontFormat
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Saving.ExportFontFormat 枚举，以便在渲染为 HTML 固定格式时实现最佳字体导出效果。提升文档的视觉质量！
type: docs
weight: 5740
url: /zh/net/aspose.words.saving/exportfontformat/
---
## ExportFontFormat enumeration

表示渲染为 HTML 固定格式时用于导出字体的格式。

```csharp
public enum ExportFontFormat
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Woff | `0` | WOFF（Web 开放字体格式）. |
| Ttf | `1` | TTF（TrueType 字体格式）. |

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

* property [FontFormat](../htmlfixedsaveoptions/fontformat/)
* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
