---
title: LayoutEnumerator.MoveLastChild
second_title: Aspose.Words for .NET API 参考
description: LayoutEnumerator 方法. 移动到最后一个子实体
type: docs
weight: 100
url: /zh/net/aspose.words.layout/layoutenumerator/movelastchild/
---
## LayoutEnumerator.MoveLastChild method

移动到最后一个子实体。

```csharp
public bool MoveLastChild()
```

### 例子

显示遍历文档布局实体的方式。

```csharp
public void LayoutEnumerator()
{
    // 打开一个包含各种布局实体的文档。
    // 布局实体是 LayoutEntityType 枚举中包含的页面、单元格、行、行和其他对象。
    // 每个布局实体在文档正文中都有一个矩形空间。
    Document doc = new Document(MyDir + "Layout entities.docx");

    // 创建一个可以像树一样遍历这些实体的枚举器。
    LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

    Assert.AreEqual(doc, layoutEnumerator.Document);

    layoutEnumerator.MoveParent(LayoutEntityType.Page);

    Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);
    Assert.Throws<InvalidOperationException>(() => Console.WriteLine(layoutEnumerator.Text));

    // 我们可以调用这个方法来确保枚举器位于第一个布局实体。
    layoutEnumerator.Reset();

    // 有两个顺序决定了布局枚举器如何继续遍历布局实体
    // 当它遇到跨越多个页面的实体时。
    // 1 - 按视觉顺序：
    // 在跨越多个页面的实体的子元素中移动时，
    // 页面布局优先，我们移动到此页面上的其他子元素并避免下一个。
    Console.WriteLine("Traversing from first to last, elements between pages separated:");
    TraverseLayoutForward(layoutEnumerator, 1);

    // 我们的枚举器现在位于集合的末尾。我们可以向后遍历布局实体以回到开头。
    Console.WriteLine("Traversing from last to first, elements between pages separated:");
    TraverseLayoutBackward(layoutEnumerator, 1);

    // 2 - 按逻辑顺序：
    // 在跨越多个页面的实体的子元素中移动时，
    // 枚举器将在页面之间移动以遍历所有子实体。
    Console.WriteLine("Traversing from first to last, elements between pages mixed:");
    TraverseLayoutForwardLogical(layoutEnumerator, 1);

    Console.WriteLine("Traversing from last to first, elements between pages mixed:");
    TraverseLayoutBackwardLogical(layoutEnumerator, 1);
}

/// <summary>
/// 通过layoutEnumerator的布局实体集合前后枚举，
/// 以深度优先的方式，并按“视觉”顺序。
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
/// 通过layoutEnumerator的布局实体集合从后到前枚举，
/// 以深度优先的方式，并按“视觉”顺序。
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
/// 通过layoutEnumerator的布局实体集合前后枚举，
/// 以深度优先的方式，并按“逻辑”顺序。
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
/// 通过layoutEnumerator的布局实体集合从后到前枚举，
/// 以深度优先的方式，并按“逻辑”顺序。
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
/// 将layoutEnumerator当前实体的信息打印到控制台，同时用制表符缩进文本
/// 基于它相对于我们在构造函数 LayoutEnumerator 实例中提供的根节点的深度。
/// 我们最后处理的矩形代表实体在文档中占据的区域和位置。
/// </summary>
private static void PrintCurrentEntity(LayoutEnumerator layoutEnumerator, int indent)
{
    string tabs = new string('\t', indent);

    Console.WriteLine(layoutEnumerator.Kind == string.Empty
        ? $"{tabs}-> Entity type: {layoutEnumerator.Type}"
        : $"{tabs}-> Entity type & kind: {layoutEnumerator.Type}, {layoutEnumerator.Kind}");

    // 只有跨度可以包含文本。
    if (layoutEnumerator.Type == LayoutEntityType.Span)
        Console.WriteLine($"{tabs}   Span contents: \"{layoutEnumerator.Text}\"");

    RectangleF leRect = layoutEnumerator.Rectangle;
    Console.WriteLine($"{tabs}   Rectangle dimensions {leRect.Width}x{leRect.Height}, X={leRect.X} Y={leRect.Y}");
    Console.WriteLine($"{tabs}   Page {layoutEnumerator.PageIndex}");
}
```

### 也可以看看

* class [LayoutEnumerator](../)
* 命名空间 [Aspose.Words.Layout](../../layoutenumerator/)
* 部件 [Aspose.Words](../../../)


