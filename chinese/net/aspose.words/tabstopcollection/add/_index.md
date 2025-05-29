---
title: TabStopCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words for .NET
description: 了解 TabStopCollection Add 方法如何有效地添加或更新制表位，从而增强文档的布局和格式。
type: docs
weight: 30
url: /zh/net/aspose.words/tabstopcollection/add/
---
## Add(*[TabStop](../../tabstop/)*) {#add}

在集合中添加或替换制表位。

```csharp
public void Add(TabStop tabStop)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| tabStop | TabStop | 要添加的制表位对象。 |

## 评论

如果指定位置已经存在制表位，则将其替换。

## 例子

展示如何向文档添加自定义制表位。

```csharp
Document doc = new Document();
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// 以下是通过“ParagraphFormat”属性将制表位添加到段落的制表位集合中的两种方法。
// 1 - 创建一个“TabStop”对象，然后将其添加到集合中：
TabStop tabStop = new TabStop(ConvertUtil.InchToPoint(3), TabAlignment.Left, TabLeader.Dashes);
paragraph.ParagraphFormat.TabStops.Add(tabStop);

// 2 - 将新制表位的属性值传递给“添加”方法：
paragraph.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(100), TabAlignment.Left,
    TabLeader.Dashes);

// 为所有段落添加 5 厘米处的制表位。
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
{
    para.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(50), TabAlignment.Left,
        TabLeader.Dashes);
}

// 每个“制表符”都会将构建器的光标移动到下一个制表位的位置。
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc.Save(ArtifactsDir + "TabStopCollection.AddTabStops.docx");
```

### 也可以看看

* class [TabStop](../../tabstop/)
* class [TabStopCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## Add(*double, [TabAlignment](../../tabalignment/), [TabLeader](../../tableader/)*) {#add_1}

在集合中添加或替换制表位。

```csharp
public void Add(double position, TabAlignment alignment, TabLeader leader)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| position | Double | 添加制表位的位置（以点为单位）。 |
| alignment | TabAlignment | 一个[`TabAlignment`](../../tabalignment/)值 that 指定制表位处的文本对齐方式。 |
| leader | TabLeader | 一个[`TabLeader`](../../tableader/)值 that 指定制表符下显示的引出线的类型。 |

## 评论

如果指定位置已经存在制表位，则将其替换。

## 例子

展示如何向文档添加自定义制表位。

```csharp
Document doc = new Document();
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// 以下是通过“ParagraphFormat”属性将制表位添加到段落的制表位集合中的两种方法。
// 1 - 创建一个“TabStop”对象，然后将其添加到集合中：
TabStop tabStop = new TabStop(ConvertUtil.InchToPoint(3), TabAlignment.Left, TabLeader.Dashes);
paragraph.ParagraphFormat.TabStops.Add(tabStop);

// 2 - 将新制表位的属性值传递给“添加”方法：
paragraph.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(100), TabAlignment.Left,
    TabLeader.Dashes);

// 为所有段落添加 5 厘米处的制表位。
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
{
    para.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(50), TabAlignment.Left,
        TabLeader.Dashes);
}

// 每个“制表符”都会将构建器的光标移动到下一个制表位的位置。
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc.Save(ArtifactsDir + "TabStopCollection.AddTabStops.docx");
```

### 也可以看看

* enum [TabAlignment](../../tabalignment/)
* enum [TabLeader](../../tableader/)
* class [TabStopCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
