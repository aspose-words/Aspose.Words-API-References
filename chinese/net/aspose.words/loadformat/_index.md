---
title: LoadFormat Enum
linktitle: LoadFormat
articleTitle: LoadFormat
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.LoadFormat 枚举，定义文档格式以实现无缝加载并增强应用程序的兼容性。
type: docs
weight: 4000
url: /zh/net/aspose.words/loadformat/
---
## LoadFormat enumeration

表示要加载的文档的格式。

```csharp
public enum LoadFormat
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Auto | `0` | 指示 Aspose.Words 自动识别格式。 |
| MsWorks | `8` | Microsoft Works 8 文档。 |
| Doc | `10` | Microsoft Word 95 或 Word 97 - 2003 文档。 |
| Dot | `11` | Microsoft Word 95 或 Word 97 - 2003 模板. |
| DocPreWord60 | `12` | 该文档为 Word 95 之前的格式。 Aspose.Words 目前不支持加载此类文档。 |
| Docx | `20` | Office Open XML WordprocessingML 文档（无宏）. |
| Docm | `21` | Office Open XML WordprocessingML 启用宏的文档。 |
| Dotx | `22` | Office Open XML WordprocessingML 模板（无宏）. |
| Dotm | `23` | Office Open XML WordprocessingML 启用宏的模板。 |
| FlatOpc | `24` | Office Open XML WordprocessingML 存储在平面 XML 文件中，而不是 ZIP 包中。 |
| FlatOpcMacroEnabled | `25` | Office Open XML WordprocessingML 启用宏的文档存储在平面 XML 文件而不是 ZIP 包中。 |
| FlatOpcTemplate | `26` | Office Open XML WordprocessingML 模板（无宏）存储在平面 XML 文件中，而不是 ZIP 包中。 |
| FlatOpcTemplateMacroEnabled | `27` | Office Open XML WordprocessingML 启用宏的模板存储在平面 XML 文件中，而不是 ZIP 包中。 |
| Rtf | `30` | RTF 格式. |
| WordML | `31` | Microsoft Word 2003 WordprocessingML 格式。 |
| Html | `50` | HTML 格式. |
| Mhtml | `51` | MHTML（Web 存档）格式。 |
| Mobi | `52` | MOBI 格式。适用于 MobiPocket 阅读器和亚马逊 Kindle 阅读器。 |
| Chm | `53` | CHM（编译的 HTML 帮助）格式。 |
| Azw3 | `54` | AZW3 格式。适用于亚马逊 Kindle 阅读器。 |
| Epub | `55` | EPUB 格式. |
| Odt | `60` | ODF 文本文档. |
| Ott | `61` | ODF 文本文档模板. |
| Text | `62` | 纯文本. |
| Markdown | `63` | Markdown 文本文档. |
| Pdf | `64` | Pdf 文档. |
| Xml | `65` | XML 文档. |
| Unknown | `255` | 无法识别的格式，无法通过 Aspose.Words 加载。 |

## 例子

展示如何将网页保存为 .docx 文件。

```csharp
const string url = "https://products.aspose.com/words/”;

using (WebClient client = new WebClient())
{
    var bytes = client.DownloadData(url);
    using (MemoryStream stream = new MemoryStream(bytes))
    {
        // URL 再次用作 baseUri，以确保正确检索任何相对图像路径。
        LoadOptions options = new LoadOptions(LoadFormat.Html, "", url);

        // 从流中加载 HTML 文档并传递 LoadOptions 对象。
        Document doc = new Document(stream, options);

        // 在此阶段，我们可以读取和编辑文档的内容，然后将其保存到本地文件系统。
        doc.Save(ArtifactsDir + "Document.InsertHtmlFromWebPage.docx");
    }
}
```

展示如何在打开 html 文档时指定基本 URI。

```csharp
// 假设我们要加载一个包含通过相对 URI 链接的图像的 .html 文档
// 但图像位于其他位置。在这种情况下，我们需要将相对 URI 解析为绝对 URI。
 // 我们可以使用 HtmlLoadOptions 对象提供基本 URI。
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// 当输入 .html 中的图像损坏时，我们的自定义基本 URI 帮助我们修复了链接。
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// 此输出文档将显示缺失的图像。
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

展示如何使用 FileFormatUtil 方法检测文档的格式。

```csharp
// 从缺少文件扩展名的文件中加载文档，然后检测其文件格式。
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

    // 以下是将 LoadFormat 转换为其对应的 SaveFormat 的两种方法。
    // 1 - 获取 LoadFormat 的文件扩展名字符串，然后从该字符串获取相应的 SaveFormat：
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 - 将 LoadFormat 直接转换为其 SaveFormat：
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // 从流中加载文档，然后将其保存到自动检测的文件扩展名。
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
