---
title: LayoutEnumerator Class
linktitle: LayoutEnumerator
articleTitle: LayoutEnumerator
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Layout.LayoutEnumerator 类，实现高效的文档布局枚举。轻松探索页面几何形状、文本和结构！
type: docs
weight: 3790
url: /zh/net/aspose.words.layout/layoutenumerator/
---
## LayoutEnumerator class

枚举文档的页面布局实体。 您可以使用此类遍历页面布局模型。可用属性包括类型、几何形状、文本和实体渲染的页面索引， 以及整体结构和关系。 使用以下组合[`GetEntity`](../layoutcollector/getentity/)和[`Current`](./current/)移动到与文档节点对应的实体。

要了解更多信息，请访问[转换为固定页面格式](https://docs.aspose.com/words/net/converting-to-fixed-page-format/)文档文章。

```csharp
public class LayoutEnumerator
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [LayoutEnumerator](layoutenumerator/)(*[Document](../../aspose.words/document/)*) | 初始化此类的新实例。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Current](../../aspose.words.layout/layoutenumerator/current/) { get; set; } | 获取或设置页面布局模型中的当前位置。 此属性返回与当前布局实体相对应的不透明对象。 |
| [Document](../../aspose.words.layout/layoutenumerator/document/) { get; } | 获取此实例枚举的文档。 |
| [Item](../../aspose.words.layout/layoutenumerator/item/) { get; } | 获取实体的命名属性。 |
| [Kind](../../aspose.words.layout/layoutenumerator/kind/) { get; } | 获取当前实体的类型。该值可以是空字符串，但不能是`无效的`. |
| [PageIndex](../../aspose.words.layout/layoutenumerator/pageindex/) { get; } | 获取包含当前实体的页面的基于 1 的索引。 |
| [Rectangle](../../aspose.words.layout/layoutenumerator/rectangle/) { get; } | 返回当前实体相对于页面左上角的边界矩形（以点为单位）。 |
| [Text](../../aspose.words.layout/layoutenumerator/text/) { get; } | 获取当前跨度实体的文本。其他实体类型抛出。 |
| [Type](../../aspose.words.layout/layoutenumerator/type/) { get; } | 获取当前实体的类型。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [MoveFirstChild](../../aspose.words.layout/layoutenumerator/movefirstchild/)() | 移动到第一个子实体。 |
| [MoveLastChild](../../aspose.words.layout/layoutenumerator/movelastchild/)() | 移动到最后一个子实体。 |
| [MoveNext](../../aspose.words.layout/layoutenumerator/movenext/)() | 按视觉顺序移动到下一个同级实体。 当迭代跨页段落的行时，此方法 不会移动到下一页，而是移动到同一页面上的下一个实体。 |
| [MoveNextLogical](../../aspose.words.layout/layoutenumerator/movenextlogical/)() | 按逻辑顺序移动到下一个同级实体。 当迭代跨页的段落行时，此方法 将移动到下一行，即使它位于另一个页面上。 |
| [MoveParent](../../aspose.words.layout/layoutenumerator/moveparent/#moveparent)() | 移动到父实体。 |
| [MoveParent](../../aspose.words.layout/layoutenumerator/moveparent/#moveparent_1)(*[LayoutEntityType](../layoutentitytype/)*) | 移动到指定类型的父实体。 |
| [MovePrevious](../../aspose.words.layout/layoutenumerator/moveprevious/)() | 移动到上一个同级实体。 |
| [MovePreviousLogical](../../aspose.words.layout/layoutenumerator/movepreviouslogical/)() | 按逻辑顺序移动到上一个同级实体。 当迭代跨页段落的行时，此方法 将移动到上一行，即使它位于另一个页面上。 |
| [Reset](../../aspose.words.layout/layoutenumerator/reset/)() | 将枚举器移动到文档的第一页。 |

## 例子

显示遍历文档布局实体的方法。

```csharp
public void LayoutEnumerator()
{
    // 打开包含多种布局实体的文档。
    // 布局实体是页面、单元格、行、线以及 LayoutEntityType 枚举中包含的其他对象。
    // 每个布局实体在文档主体中占据一个矩形空间。
    Document doc = new Document(MyDir + "Layout entities.docx");

    // 创建一个可以像树一样遍历这些实体的枚举器。
    LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

    Assert.AreEqual(doc, layoutEnumerator.Document);

    layoutEnumerator.MoveParent(LayoutEntityType.Page);

    Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);
    Assert.Throws<InvalidOperationException>(() => Console.WriteLine(layoutEnumerator.Text));

    // 我们可以调用此方法来确保枚举器位于第一个布局实体。
    layoutEnumerator.Reset();

    // 有两种顺序决定布局枚举器如何继续遍历布局实体
    // 当遇到跨越多个页面的实体时。
    // 1 - 按视觉顺序：
    // 当跨多个页面移动实体的子实体时，
    // 页面布局优先，我们移动到此页面上的其他子元素并避开下一页的子元素。
    Console.WriteLine("Traversing from first to last, elements between pages separated:");
    TraverseLayoutForward(layoutEnumerator, 1);

    // 我们的枚举器现在位于集合的末尾。我们可以反向遍历布局实体，回到集合的开头。
    Console.WriteLine("Traversing from last to first, elements between pages separated:");
    TraverseLayoutBackward(layoutEnumerator, 1);

    // 2 - 按逻辑顺序：
    // 当跨多个页面移动实体的子实体时，
    // 枚举器将在页面之间移动以遍历所有子实体。
    Console.WriteLine("Traversing from first to last, elements between pages mixed:");
    TraverseLayoutForwardLogical(layoutEnumerator, 1);

    Console.WriteLine("Traversing from last to first, elements between pages mixed:");
    TraverseLayoutBackwardLogical(layoutEnumerator, 1);
}

/// <summary>
/// 从前到后枚举layoutEnumerator的布局实体集合，
/// 以深度优先的方式，按照“视觉”顺序。
/// </summary>
private static void TraverseLayoutForward(LayoutEnumerator layoutEnumerator, int depth)
{
    do
    {
        PrintCurrentEntity(layoutEnumerator, depth);

        if (layoutEnumerator.MoveFirstChild())
        {
            TraverseLayoutForward(layoutEnumerator, depth + 1);
            layoutEnumerator.MoveParent();
        }
    } while (layoutEnumerator.MoveNext());
}

/// <summary>
/// 从后到前遍历layoutEnumerator的布局实体集合，
/// 以深度优先的方式，按照“视觉”顺序。
/// </summary>
private static void TraverseLayoutBackward(LayoutEnumerator layoutEnumerator, int depth)
{
    do
    {
        PrintCurrentEntity(layoutEnumerator, depth);

        if (layoutEnumerator.MoveLastChild())
        {
            TraverseLayoutBackward(layoutEnumerator, depth + 1);
            layoutEnumerator.MoveParent();
        }
    } while (layoutEnumerator.MovePrevious());
}

/// <summary>
/// 从前到后枚举layoutEnumerator的布局实体集合，
/// 以深度优先的方式，并按照“逻辑”顺序。
/// </summary>
private static void TraverseLayoutForwardLogical(LayoutEnumerator layoutEnumerator, int depth)
{
    do
    {
        PrintCurrentEntity(layoutEnumerator, depth);

        if (layoutEnumerator.MoveFirstChild())
        {
            TraverseLayoutForwardLogical(layoutEnumerator, depth + 1);
            layoutEnumerator.MoveParent();
        }
    } while (layoutEnumerator.MoveNextLogical());
}

/// <summary>
/// 从后到前遍历layoutEnumerator的布局实体集合，
/// 以深度优先的方式，并按照“逻辑”顺序。
/// </summary>
private static void TraverseLayoutBackwardLogical(LayoutEnumerator layoutEnumerator, int depth)
{
    do
    {
        PrintCurrentEntity(layoutEnumerator, depth);

        if (layoutEnumerator.MoveLastChild())
        {
            TraverseLayoutBackwardLogical(layoutEnumerator, depth + 1);
            layoutEnumerator.MoveParent();
        }
    } while (layoutEnumerator.MovePreviousLogical());
}

/// <summary>
/// 将有关layoutEnumerator当前实体的信息打印到控制台，同时使用制表符缩进文本
/// 基于我们在构造函数 LayoutEnumerator 实例中提供的相对于根节点的深度。
/// 我们最后处理的矩形代表实体在文档中占据的区域和位置。
/// </summary>
private static void PrintCurrentEntity(LayoutEnumerator layoutEnumerator, int indent)
{
    string tabs = new string('\t', indent);

    Console.WriteLine(layoutEnumerator.Kind == string.Empty
        ? $"{tabs}-> Entity type: {layoutEnumerator.Type}"
        : $"{tabs}-> Entity type & kind: {layoutEnumerator.Type}, {layoutEnumerator.Kind}");

    // 只有 span 可以包含文本。
    if (layoutEnumerator.Type == LayoutEntityType.Span)
        Console.WriteLine($"{tabs}   Span contents: \"{layoutEnumerator.Text}\"");

    RectangleF leRect = layoutEnumerator.Rectangle;
    Console.WriteLine($"{tabs}   Rectangle dimensions {leRect.Width}x{leRect.Height}, X={leRect.X} Y={leRect.Y}");
    Console.WriteLine($"{tabs}   Page {layoutEnumerator.PageIndex}");
}
```

### 也可以看看

* 命名空间 [Aspose.Words.Layout](../../aspose.words.layout/)
* 部件 [Aspose.Words](../../)
