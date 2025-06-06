---
title: WarningSource Enum
linktitle: WarningSource
articleTitle: WarningSource
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.WarningSource 枚举，识别文档加载和保存期间的警告源，以增强文档管理。
type: docs
weight: 7500
url: /zh/net/aspose.words/warningsource/
---
## WarningSource enumeration

指定在文档加载或保存期间产生警告的模块。

```csharp
public enum WarningSource
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Unknown | `0` | 未指定警告源。 |
| Layout | `1` | 构建文档布局的模块。 |
| DrawingML | `2` | 渲染 DrawingML 形状的模块。 |
| OfficeMath | `3` | 渲染 OfficeMath 的模块。 |
| Shapes | `4` | 渲染普通形状的模块。 |
| Metafile | `5` | 渲染元文件的模块。 |
| Xps | `6` | 渲染 XPS 的模块。 |
| Pdf | `7` | 渲染 PDF 的模块。 |
| Image | `8` | 渲染图像的模块。 |
| Docx | `9` | 读取/写入 DOCX 文件的模块。 |
| Doc | `10` | 读取/写入二进制 DOC 文件的模块。 |
| Text | `11` | 读取/写入纯文本文件的模块。 |
| Rtf | `12` | 读取/写入 RTF 文件的模块。 |
| WordML | `13` | 读取/写入 WML 文件的模块。 |
| Nrx | `14` | DOCX/WML 阅读器/编写器模块之间共享的通用模块。 |
| Odt | `15` | 读取/写入 ODT 文件的模块。 |
| Html | `16` | 读取/写入 HTML/MHTML 文件的模块。 |
| Validator | `17` | 验证模型一致性和有效性的模块。 |
| Xaml | `18` | 读取/写入 Xaml 文件的模块。 |
| Svm | `19` | 读取 Svm 文件的模块。 |
| MathML | `20` | 读取 W3C MathML 文件的模块。 |
| Font | `21` | 读取字体文件的模块。 |
| Svg | `22` | 读取 SVG 文件的模块。 |
| Markdown | `23` | 读取/写入 Markdown 文件的模块。 |
| Chm | `24` | 读取 CHM 文件的模块。 |
| Epub | `25` | 读取/写入 EPUB 文件的模块。 |
| Xml | `26` | 读取 XML 文件的模块。 |
| Xlsx | `27` | 写入 XLSX 文件的模块。 |

## 例子

展示如何使用警告源。

```csharp
Document doc = new Document(MyDir + "Emphases markdown warning.docx");

WarningInfoCollection warnings = new WarningInfoCollection();
doc.WarningCallback = warnings;
doc.Save(ArtifactsDir + "DocumentBuilder.EmphasesWarningSourceMarkdown.md");

foreach (WarningInfo warningInfo in warnings)
{
    if (warningInfo.Source == WarningSource.Markdown)
        Assert.AreEqual("The (*, 0:11) cannot be properly written into Markdown.", warningInfo.Description);
}
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
