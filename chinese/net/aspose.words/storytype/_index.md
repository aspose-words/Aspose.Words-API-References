---
title: StoryType Enum
linktitle: StoryType
articleTitle: StoryType
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.StoryType 枚举，轻松高效地管理 Word 文档文本故事。立即提升您的文档处理体验！
type: docs
weight: 6970
url: /zh/net/aspose.words/storytype/
---
## StoryType enumeration

Word 文档的文本存储在故事中。`StoryType`识别一个故事。

```csharp
public enum StoryType
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `0` | 默认值。文档中没有此故事。 |
| MainText | `1` | 包含文档的正文，表示为[`Body`](../body/). |
| Footnotes | `2` | 包含脚注文本，表示为[`Footnote`](../../aspose.words.notes/footnote/). |
| Endnotes | `3` | 包含尾注文本，表示为[`Footnote`](../../aspose.words.notes/footnote/). |
| Comments | `4` | 包含文档注释（注解），表示为[`Comment`](../comment/). |
| Textbox | `5` | 包含形状或文本框文本，表示为[`Shape`](../../aspose.words.drawing/shape/). |
| EvenPagesHeader | `6` | 包含偶数页页眉的文本，表示为[`HeaderFooter`](../headerfooter/). |
| PrimaryHeader | `7` | 包含主页眉文本。当奇数页和偶数页的页眉不同时， 包含奇数页页眉文本。表示为[`HeaderFooter`](../headerfooter/). |
| EvenPagesFooter | `8` | 包含偶数页页脚的文本，表示为[`HeaderFooter`](../headerfooter/). |
| PrimaryFooter | `9` | 包含主页脚文本。当奇数页和偶数页的页脚不同时， 包含奇数页页脚文本。表示为[`HeaderFooter`](../headerfooter/). |
| FirstPageHeader | `10` | 包含第一页页眉的文本，表示为[`HeaderFooter`](../headerfooter/). |
| FirstPageFooter | `11` | 包含第一页页脚的文本，表示为[`HeaderFooter`](../headerfooter/). |
| FootnoteSeparator | `12` | 包含脚注分隔符的文本。 |
| FootnoteContinuationSeparator | `13` | 包含脚注延续分隔符的文本。 |
| FootnoteContinuationNotice | `14` | 包含脚注延续通知分隔符的文本。 |
| EndnoteSeparator | `15` | 包含尾注分隔符的文本。 |
| EndnoteContinuationSeparator | `16` | 包含尾注延续分隔符的文本。 |
| EndnoteContinuationNotice | `17` | 包含尾注延续通知分隔符的文本。 |

## 例子

展示如何从节点中删除所有形状。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 使用 DocumentBuilder 插入形状。这是一个内联形状，
// 它有一个父段落，它是第一节正文的子节点。
builder.InsertShape(ShapeType.Cube, 100.0, 100.0);

Assert.AreEqual(1, doc.GetChildNodes(NodeType.Shape, true).Count);

// 我们可以从这个主体的子段落中删除所有形状。
Assert.AreEqual(StoryType.MainText, doc.FirstSection.Body.StoryType);
doc.FirstSection.Body.DeleteShapes();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
