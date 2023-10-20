---
title: LayoutEnumerator.MoveNextLogical
linktitle: MoveNextLogical
articleTitle: MoveNextLogical
second_title: Aspose.Words для .NET
description: LayoutEnumerator MoveNextLogical метод. Переходит к следующему одноуровневому объекту в логическом порядке. При повторении строк абзаца разбитого на страницы этот метод перейдет к следующей строке даже если он находится на другой странице на С#.
type: docs
weight: 130
url: /ru/net/aspose.words.layout/layoutenumerator/movenextlogical/
---
## LayoutEnumerator.MoveNextLogical method

Переходит к следующему одноуровневому объекту в логическом порядке. При повторении строк абзаца, разбитого на страницы, этот метод перейдет к следующей строке, даже если он находится на другой странице.

```csharp
public bool MoveNextLogical()
```

## Примечания

Обратите внимание, что всеSpan сущности связаны друг с другом, таким образом, если[`Current`](../current/) Сущность представляет собой интервал повторного вызова этого метода, который будет повторять всю историю документа.

## Примеры

Показывает способы перемещения по объектам макета документа.

```csharp
public void LayoutEnumerator()
{
    // Открытие документа, содержащего различные объекты макета.
    // Сущностями макета являются страницы, ячейки, строки, строки и другие объекты, включенные в перечисление LayoutEntityType.
    // Каждый объект макета имеет прямоугольное пространство, которое он занимает в теле документа.
    Document doc = new Document(MyDir + "Layout entities.docx");

    // Создаем перечислитель, который может перемещаться по этим объектам, как по дереву.
    LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

    Assert.AreEqual(doc, layoutEnumerator.Document);

    layoutEnumerator.MoveParent(LayoutEntityType.Page);

    Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);
    Assert.Throws<InvalidOperationException>(() => Console.WriteLine(layoutEnumerator.Text));

    // Мы можем вызвать этот метод, чтобы убедиться, что перечислитель находится в первом объекте макета.
    layoutEnumerator.Reset();

    // Есть два порядка, которые определяют, как перечислитель макета продолжает обходить объекты макета
    // когда он сталкивается с объектами, охватывающими несколько страниц.
    // 1 - В визуальном порядке:
    // При перемещении по дочерним элементам сущности, занимающим несколько страниц,
    // Макет страницы имеет приоритет, и мы переходим к другим дочерним элементам на этой странице и избегаем элементов на следующей.
    Console.WriteLine("Traversing from first to last, elements between pages separated:");
    TraverseLayoutForward(layoutEnumerator, 1);

    // Наш перечислитель теперь находится в конце коллекции. Мы можем перемещаться по объектам макета назад, чтобы вернуться к началу.
    Console.WriteLine("Traversing from last to first, elements between pages separated:");
    TraverseLayoutBackward(layoutEnumerator, 1);

    // 2 - В логическом порядке:
    // При перемещении по дочерним элементам сущности, занимающим несколько страниц,
    // перечислитель будет перемещаться между страницами, чтобы пройти по всем дочерним объектам.
    Console.WriteLine("Traversing from first to last, elements between pages mixed:");
    TraverseLayoutForwardLogical(layoutEnumerator, 1);

    Console.WriteLine("Traversing from last to first, elements between pages mixed:");
    TraverseLayoutBackwardLogical(layoutEnumerator, 1);
}

/// <summary>
/// Перечисляем коллекцию сущностей макета LayoutEnumerator от начала до конца,
/// в порядке глубины и в «визуальном» порядке.
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
/// Перечисляем коллекцию объектов макета LayoutEnumerator задом наперед,
/// в порядке глубины и в «визуальном» порядке.
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
/// Перечисляем коллекцию сущностей макета LayoutEnumerator от начала до конца,
/// в глубину и в «логическом» порядке.
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
/// Перечисляем коллекцию объектов макета LayoutEnumerator задом наперед,
/// в глубину и в «логическом» порядке.
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
/// Выводим информацию о текущей сущности LayoutEnumerator на консоль, делая отступы для текста с помощью символов табуляции
/// на основе его глубины относительно корневого узла, который мы предоставили в экземпляре конструктора LayoutEnumerator.
/// Прямоугольник, который мы обрабатываем в конце, представляет область и местоположение, которое объект занимает в документе.
/// </summary>
private static void PrintCurrentEntity(LayoutEnumerator layoutEnumerator, int indent)
{
    string tabs = new string('\t', indent);

    Console.WriteLine(layoutEnumerator.Kind == string.Empty
        ? $"{tabs}-> Entity type: {layoutEnumerator.Type}"
        : $"{tabs}-> Entity type & kind: {layoutEnumerator.Type}, {layoutEnumerator.Kind}");

    // Только промежутки могут содержать текст.
    if (layoutEnumerator.Type == LayoutEntityType.Span)
        Console.WriteLine($"{tabs}   Span contents: \"{layoutEnumerator.Text}\"");

    RectangleF leRect = layoutEnumerator.Rectangle;
    Console.WriteLine($"{tabs}   Rectangle dimensions {leRect.Width}x{leRect.Height}, X={leRect.X} Y={leRect.Y}");
    Console.WriteLine($"{tabs}   Page {layoutEnumerator.PageIndex}");
}
```

### Смотрите также

* class [LayoutEnumerator](../)
* пространство имен [Aspose.Words.Layout](../../../aspose.words.layout/)
* сборка [Aspose.Words](../../../)
