---
title: ImportFormatOptions.IgnoreHeaderFooter
linktitle: IgnoreHeaderFooter
articleTitle: IgnoreHeaderFooter
second_title: Aspose.Words for .NET
description: 探索 ImportFormatOptions 的 IgnoreHeaderFooter 属性，在 KeepSourceFormatting 模式下控制页眉/页脚的格式。立即简化您的文档导入！
type: docs
weight: 40
url: /zh/net/aspose.words/importformatoptions/ignoreheaderfooter/
---
## ImportFormatOptions.IgnoreHeaderFooter property

获取或设置一个布尔值，该值指定页眉/页脚内容的源格式是否被忽略 KeepSourceFormatting模式。 默认值为`真的`.

```csharp
public bool IgnoreHeaderFooter { get; set; }
```

## 例子

展示如何指定忽略或不忽略页眉/页脚内容的源格式。

```csharp
Document dstDoc = new Document(MyDir + "Document.docx");
Document srcDoc = new Document(MyDir + "Header and footer types.docx");

// 如果“IgnoreHeaderFooter”为假，则页眉/页脚内容的原始格式
// 将使用来自“页眉和页脚类型.docx”的内容。
// 如果“IgnoreHeaderFooter”为真，则页眉/页脚内容的格式
// 将使用来自“Document.docx”的内容。
ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.IgnoreHeaderFooter = false;

dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, importFormatOptions);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.DoNotIgnoreHeaderFooter.docx");
```

### 也可以看看

* class [ImportFormatOptions](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
