---
title: LayoutEnumerator Class
linktitle: LayoutEnumerator
articleTitle: LayoutEnumerator
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Layout.LayoutEnumerator 班级. 枚举文档的页面布局实体 您可以使用此类来遍历页面布局模型可用属性包括类型几何形状文本和呈现实体的页面索引 以及整体结构和关系 使用以下组合GetEntity和Current移动到对应于文档节点的实体 在 C#.
type: docs
weight: 3340
url: /zh/net/aspose.words.layout/layoutenumerator/
---
## LayoutEnumerator class

枚举文档的页面布局实体。 您可以使用此类来遍历页面布局模型。可用属性包括类型、几何形状、文本和呈现实体的页面索引， 以及整体结构和关系。 使用以下组合[`GetEntity`](../layoutcollector/getentity/)和[`Current`](./current/)移动到对应于文档节点的实体。

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
| [Kind](../../aspose.words.layout/layoutenumerator/kind/) { get; } | 获取当前实体的种类。这可以是空字符串，但绝不能`无效的`. |
| [PageIndex](../../aspose.words.layout/layoutenumerator/pageindex/) { get; } | 获取包含当前实体的页面的从 1 开始的索引。 |
| [Rectangle](../../aspose.words.layout/layoutenumerator/rectangle/) { get; } | 返回当前实体相对于页面左上角的边界矩形（以磅为单位）。 |
| [Text](../../aspose.words.layout/layoutenumerator/text/) { get; } | 获取当前跨度实体的文本。其他实体类型的抛出异常。 |
| [Type](../../aspose.words.layout/layoutenumerator/type/) { get; } | 获取当前实体的类型。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [MoveFirstChild](../../aspose.words.layout/layoutenumerator/movefirstchild/)() | 移动到第一个子实体。 |
| [MoveLastChild](../../aspose.words.layout/layoutenumerator/movelastchild/)() | 移动到最后一个子实体。 |
| [MoveNext](../../aspose.words.layout/layoutenumerator/movenext/)() | 按视觉顺序移动到下一个同级实体。 当迭代跨页的段落行时，此方法 不会移动到下一页，而是移动到同一页面上的下一个实体。 |
| [MoveNextLogical](../../aspose.words.layout/layoutenumerator/movenextlogical/)() | 按逻辑顺序移动到下一个同级实体。 当迭代跨页的段落行时，此方法 将移动到下一行，即使它驻留在另一页上。 |
| [MoveParent](../../aspose.words.layout/layoutenumerator/moveparent/#moveparent)() | 移动到父实体。 |
| [MoveParent](../../aspose.words.layout/layoutenumerator/moveparent/#moveparent_1)(*[LayoutEntityType](../layoutentitytype/)*) | 移动到指定类型的父实体。 |
| [MovePrevious](../../aspose.words.layout/layoutenumerator/moveprevious/)() | 移动到上一个同级实体。 |
| [MovePreviousLogical](../../aspose.words.layout/layoutenumerator/movepreviouslogical/)() | 按逻辑顺序移动到上一个同级实体。 当迭代跨页的段落行时，此方法 将移动到上一行，即使它驻留在另一页上。 |
| [Reset](../../aspose.words.layout/layoutenumerator/reset/)() | 将枚举器移至文档的第一页。 |

## 例子

显示遍历文档布局实体的方法。

```csharp
public void LayoutEnumerator()
{
    // 打开包含各种布局实体的文档。
    // 布局实体是页面、单元格、行、线以及 LayoutEntityType 枚举中包含的其他对象。
    // 每个布局实体在文档正文中都有一个占据的矩形空间。
    Document doc = new Document(MyDir + "Layout entities.docx");

    // 创建一个枚举器，可以像树一样遍历这些实体。
    LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

    Assert.AreEqual(doc, layoutEnumerator.Document);

    layoutEnumerator.MoveParent(LayoutEntityType.Page);

    Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);
    Assert.Throws<InvalidOperationException>(() => Console.WriteLine(layoutEnumerator.Text));

    // 我们可以调用此方法来确保枚举器位于第一个布局实体。
    layoutEnumerator.Reset();

    // 有两个顺序决定布局枚举器如何继续遍历布局实体
    // 当遇到跨多个页面的实体时。
    // 1 - 按视觉顺序：
    // 当在跨多个页面的实体子级之间移动时，
    // 页面布局优先，我们移动到此页面上的其他子元素并避免下一个页面上的子元素。
    Console.WriteLine("Traversing from first to last, elements between pages separated:");
    TraverseLayoutForward(layoutEnumerator, 1);

    // 我们的枚举器现在位于集合的末尾。我们可以向后遍历布局实体以回到开头。
    Console.WriteLine("Traversing from last to first, elements between pages separated:");
    TraverseLayoutBackward(layoutEnumerator, 1);

    // 2 - 按逻辑顺序：
    // 当在跨多个页面的实体子级之间移动时，
    // 枚举器将在页面之间移动以遍历所有子实体。
    Console.WriteLine("Traversing from first to last, elements between pages mixed:");
    TraverseLayoutForwardLogical(layoutEnumerator, 1);

    Console.WriteLine("Traversing from last to first, elements between pages mixed:");
    TraverseLayoutBackwardLogical(layoutEnumerator, 1);
}

/// <summary>
/// 通过layoutEnumerator的布局实体集合从前到后枚举，
/// 以深度优先的方式，并按照“视觉”顺序。
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
/// 通过layoutEnumerator的布局实体集合从后往前枚举，
/// 以深度优先的方式，并按照“视觉”顺序。
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
/// 通过layoutEnumerator的布局实体集合从前到后枚举，
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
/// 通过layoutEnumerator的布局实体集合从后往前枚举，
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
/// 将layoutEnumerator当前实体的信息打印到控制台，同时使用制表符缩进文本
/// 基于其相对于我们在构造函数 LayoutEnumerator 实例中提供的根节点的深度。
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
