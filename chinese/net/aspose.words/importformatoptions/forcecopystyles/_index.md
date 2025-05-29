---
title: ImportFormatOptions.ForceCopyStyles
linktitle: ForceCopyStyles
articleTitle: ForceCopyStyles
second_title: Aspose.Words for .NET
description: 探索 ImportFormatOptions ForceCopyStyles 属性，轻松控制 KeepSourceFormatting 模式下的样式复制。默认值为 false，以获得最佳效果。
type: docs
weight: 30
url: /zh/net/aspose.words/importformatoptions/forcecopystyles/
---
## ImportFormatOptions.ForceCopyStyles property

获取或设置一个布尔值，指示是否复制冲突的样式 KeepSourceFormatting mode. 默认值为`错误的`.

```csharp
public bool ForceCopyStyles { get; set; }
```

## 评论

默认情况下，如果目标文档中已经存在匹配的样式，则源样式 formatting 将扩展为直接节点属性，并将该节点的样式重置为默认值。

当此选项设置为`真的`，源样式将被强制复制 到具有唯一名称的目标文档中并应用于导入的节点。

请注意，在这种情况下，不能保证目标 document 中导入节点的格式会被保留。

## 例子

展示如何强制复制具有唯一名称的源样式。

```csharp
// 两个文档都包含 MyStyle1 和 MyStyle2，MyStyle3 仅存在于源文档中。
Document srcDoc = new Document(MyDir + "Styles source.docx");
Document dstDoc = new Document(MyDir + "Styles destination.docx");

ImportFormatOptions options = new ImportFormatOptions { ForceCopyStyles = true };
dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

ParagraphCollection paras = dstDoc.Sections[1].Body.Paragraphs;

Assert.AreEqual(paras[0].ParagraphFormat.Style.Name, "MyStyle1_0");
Assert.AreEqual(paras[1].ParagraphFormat.Style.Name, "MyStyle2_0");
Assert.AreEqual(paras[2].ParagraphFormat.Style.Name, "MyStyle3");
```

### 也可以看看

* class [ImportFormatOptions](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
