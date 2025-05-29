---
title: ParagraphFormat.WidowControl
linktitle: WidowControl
articleTitle: WidowControl
second_title: Aspose.Words for .NET
description: 了解 ParagraphFormat WidowControl 属性如何确保文本的第一行和最后一行保持在同一页面上，以提高可读性。
type: docs
weight: 410
url: /zh/net/aspose.words/paragraphformat/widowcontrol/
---
## ParagraphFormat.WidowControl property

如果段落的第一行和最后一行要与段落的其余部分保留在同一页面上，则为真。

```csharp
public bool WidowControl { get; set; }
```

## 例子

展示如何启用段落的孤行/寡行控制。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 当我们编写不适合放在一页上的文本时，一行可能会溢出到下一页。
// 下一页的单行被称为“孤行”，
// 并且孤行断开的上一行被称为“寡妇”。
// 我们可以通过字体大小、间距或页边距重新排列文本来修复孤行和寡行。
// 如果我们希望保留文档的尺寸，我们可以将此标志设置为“true”
// 将寡妇推到与各自的孤儿相同的页面上。
// 将此标志保留为“false”将在文本中留下寡妇/孤儿对。
// 每个段落都可以在 Microsoft Word 中通过“主页”->“段落”->“段落设置”访问此设置
//（“段落”选项卡右下角的按钮）->“寡妇/孤儿控制”。
builder.ParagraphFormat.WidowControl = widowControl; 

// 插入产生孤儿和寡妇的文本。
builder.Font.Size = 68;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "ParagraphFormat.WidowControl.docx");
```

### 也可以看看

* class [ParagraphFormat](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
