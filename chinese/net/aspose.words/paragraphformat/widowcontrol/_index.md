---
title: ParagraphFormat.WidowControl
second_title: Aspose.Words for .NET API 参考
description: ParagraphFormat 财产. 如果段落中的第一行和最后一行与段落的其余部分保留在同一页上则为 True
type: docs
weight: 400
url: /zh/net/aspose.words/paragraphformat/widowcontrol/
---
## ParagraphFormat.WidowControl property

如果段落中的第一行和最后一行与段落的其余部分保留在同一页上，则为 True。

```csharp
public bool WidowControl { get; set; }
```

### 例子

演示如何启用段落的寡妇/孤儿控制。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 当我们编写一页放不下的文本时，一行可能会溢出到下一页。
// 在下一页结束的单行称为“孤行”，
// 孤儿中断的前一行称为“寡妇”。
// 我们可以通过字体大小、间距或页边距重新排列文本来修复孤儿和寡妇。
// 如果我们希望保留文档的尺寸，我们可以将此标志设置为“true”
 // 将寡妇推到与其各自的孤儿相同的页面上。
// 将此标志保留为“false”将在文本中留下寡妇/孤儿对。
// 每个段落都可以在 Microsoft Word 中通过 Home -> 访问此设置段落->段落设置
//（“段落”选项卡右下角的按钮）-> “寡妇/孤儿控制”。
builder.ParagraphFormat.WidowControl = widowControl; 

// 插入产生孤儿和寡妇的文本。
builder.Font.Size = 68;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "ParagraphFormat.WidowControl.docx");
```

### 也可以看看

* class [ParagraphFormat](../)
* 命名空间 [Aspose.Words](../../paragraphformat/)
* 部件 [Aspose.Words](../../../)


