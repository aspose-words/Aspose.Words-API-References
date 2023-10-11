---
title: Enum ExportFontFormat
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Saving.ExportFontFormat 枚举. 表示渲染为 HTML 固定格式时用于导出字体的格式
type: docs
weight: 4990
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
| Woff | `0` | WOFF（网络开放字体格式）. |
| Ttf | `1` | TTF（TrueType 字体格式）. |

### 例子

显示将文档保存为 HTML 时如何仅使用目标计算机的字体。

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


