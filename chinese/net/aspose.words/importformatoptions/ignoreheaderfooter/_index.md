---
title: ImportFormatOptions.IgnoreHeaderFooter
linktitle: IgnoreHeaderFooter
articleTitle: IgnoreHeaderFooter
second_title: 用于 .NET 的 Aspose.Words
description: ImportFormatOptions IgnoreHeaderFooter 财产. 获取或设置一个布尔值该值指定忽略页眉/页脚内容的源格式 ifKeepSourceFormatting使用模式 默认值为真的 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words/importformatoptions/ignoreheaderfooter/
---
## ImportFormatOptions.IgnoreHeaderFooter property

获取或设置一个布尔值，该值指定忽略页眉/页脚内容的源格式 ifKeepSourceFormatting使用模式。 默认值为`真的`.

```csharp
public bool IgnoreHeaderFooter { get; set; }
```

## 例子

演示如何指定忽略或不忽略页眉/页脚内容的源格式。

```csharp
Document dstDoc = new Document(MyDir + "Document.docx");
Document srcDoc = new Document(MyDir + "Header and footer types.docx");

ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.IgnoreHeaderFooter = false;

dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, importFormatOptions);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.DoNotIgnoreHeaderFooter.docx");
```

### 也可以看看

* class [ImportFormatOptions](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
