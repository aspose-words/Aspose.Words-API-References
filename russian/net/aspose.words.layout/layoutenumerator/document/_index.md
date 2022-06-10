---
title: Document
second_title: Справочник по API Aspose.Words для .NET
description: Получает документ перечисляемый этим экземпляром.
type: docs
weight: 30
url: /ru/net/aspose.words.layout/layoutenumerator/document/
---
## LayoutEnumerator.Document property

Получает документ, перечисляемый этим экземпляром.

```csharp
public Document Document { get; }
```

### Примеры

Показывает способы обхода объектов макета документа.

```csharp
public void LayoutEnumerator()
{
     // Открытие документа, содержащего множество объектов макета.
     // Объектами макета являются страницы, ячейки, строки, строки и другие объекты, включенные в перечисление LayoutEntityType.
     // Каждый объект макета имеет прямоугольное пространство, которое он занимает в теле документа.
    Document doc = new Document(MyDir + "Layout entities.docx");

     // Создаем перечислитель, который может проходить по этим объектам, как по дереву.
    LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

    Assert.AreEqual(doc, layoutEnumerator.Document);

    layoutEnumerator.MoveParent(LayoutEntityType.Page);

    Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);
    Assert.Throws<InvalidOperationException>(() => Console.WriteLine(layoutEnumerator.Text));

     // Мы можем вызвать этот метод, чтобы убедиться, что перечислитель будет находиться на первом объекте макета.
    layoutEnumerator.Reset();

     // Есть два порядка, которые определяют, как перечислитель макета продолжает обход макета entity
     // когда он сталкивается с объектами, которые охватывают несколько страниц.
     // 1 - В визуальном порядке: 
     // При перемещении по дочерним объектам, которые охватывают несколько страниц, 
    // макет страницы имеет приоритет, и мы переходим к другим дочерним элементам на этой странице и избегаем элементов на следующей.
    Console.WriteLine("Traversing from first to last, elements between pages separated:");
    TraverseLayoutForward(layoutEnumerator, 1);

     // Наш перечислитель теперь находится в конце коллекции. Мы можем пройти по объектам макета назад, чтобы вернуться к началу.
    Console.WriteLine("Traversing from last to first, elements between pages separated:");
    TraverseLayoutBackward(layoutEnumerator, 1);

     // 2 - В логическом порядке: 
     // При перемещении по дочерним объектам, которые охватывают несколько страниц, 
     // перечислитель будет перемещаться между страницами для обхода всех дочерних объектов.
    Console.WriteLine("Traversing from first to last, elements between pages mixed:");
    TraverseLayoutForwardLogical(layoutEnumerator, 1);

    Console.WriteLine("Traversing from last to first, elements between pages mixed:");
    TraverseLayoutBackwardLogical(layoutEnumerator, 1);
}

/// <summary>
 /// Перечислить коллекцию сущностей макета layoutEnumerator от начала до конца, 
 /// в глубину и в "визуальном" порядке.
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
 /// Перебор коллекции сущностей макета layoutEnumerator в обратном порядке, 
 /// в глубину и в "визуальном" порядке.
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
 /// Перечислить коллекцию сущностей макета layoutEnumerator от начала до конца, 
 /// в глубину и в "логическом" порядке.
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
 /// Перебор коллекции сущностей макета layoutEnumerator в обратном порядке, 
 /// в глубину и в "логическом" порядке.
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
 /// Выводим информацию о текущем объекте layoutEnumerator в консоль, при этом отступ текста с табуляцией character
 /// на основе его глубины относительно корневого узла, который мы указали в конструкторе LayoutEnumerator instance.
/// Прямоугольник, который мы обрабатываем в конце, представляет собой область и местоположение, которое объект занимает в документе.
/// </summary>
private static void PrintCurrentEntity(LayoutEnumerator layoutEnumerator, int indent)
{
    string tabs = new string('\t', indent);

    Console.WriteLine(layoutEnumerator.Kind == string.Empty
        ? $"{tabs}-> Entity type: {layoutEnumerator.Type}"
        : $"{tabs}-> Entity type & kind: {layoutEnumerator.Type}, {layoutEnumerator.Kind}");

     // Только диапазоны могут содержать текст.
    if (layoutEnumerator.Type == LayoutEntityType.Span)
        Console.WriteLine($"{tabs}   Span contents: \"{layoutEnumerator.Text}\"");

    RectangleF leRect = layoutEnumerator.Rectangle;
    Console.WriteLine($"{tabs}   Rectangle dimensions {leRect.Width}x{leRect.Height}, X={leRect.X} Y={leRect.Y}");
    Console.WriteLine($"{tabs}   Page {layoutEnumerator.PageIndex}");
}
```

### Смотрите также

* class [Document](../../../aspose.words/document)
* class [LayoutEnumerator](../../layoutenumerator)
* пространство имен [Aspose.Words.Layout](../../layoutenumerator)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
