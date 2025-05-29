---
title: ParagraphFormat.LinesToDrop
linktitle: LinesToDrop
articleTitle: LinesToDrop
second_title: Aspose.Words for .NET
description: 了解 ParagraphFormat LinesToDrop 属性如何增强文档中的首字下沉高度。优化您的文本布局，打造惊艳视觉效果！
type: docs
weight: 210
url: /zh/net/aspose.words/paragraphformat/linestodrop/
---
## ParagraphFormat.LinesToDrop property

获取或设置用于计算首字下沉高度的段落文本行数。

```csharp
public int LinesToDrop { get; set; }
```

## 例子

展示如何设置首字下沉的大小。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 修改“LinesToDrop”属性以将段落指定为首字下沉，
// 这会将其变成一个大写字母，用于装饰下一段。
// 赋予此属性值 4，使首字下沉具有四行文本的高度。
builder.ParagraphFormat.LinesToDrop = 4;
builder.Writeln("H");

// 将“LinesToDrop”属性重置为 0，以将下一个段落变成普通段落。
// 本段文字将环绕首字下沉。
builder.ParagraphFormat.LinesToDrop = 0;
builder.Writeln("ello world!");

doc.Save(ArtifactsDir + "ParagraphFormat.LinesToDrop.odt");
```

### 也可以看看

* class [ParagraphFormat](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
