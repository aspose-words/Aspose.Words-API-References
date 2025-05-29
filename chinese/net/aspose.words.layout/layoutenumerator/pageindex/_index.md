---
title: LayoutEnumerator.PageIndex
linktitle: PageIndex
articleTitle: PageIndex
second_title: Aspose.Words for .NET
description: 探索 LayoutEnumerator 的 PageIndex 属性。轻松检索包含当前实体的页面的从 1 开始的索引，实现无缝导航。
type: docs
weight: 60
url: /zh/net/aspose.words.layout/layoutenumerator/pageindex/
---
## LayoutEnumerator.PageIndex property

获取包含当前实体的页面的基于 1 的索引。

```csharp
public int PageIndex { get; }
```

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

* class [LayoutEnumerator](../)
* 命名空间 [Aspose.Words.Layout](../../../aspose.words.layout/)
* 部件 [Aspose.Words](../../../)
