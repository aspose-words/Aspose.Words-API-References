---
title: LayoutEnumerator Class
linktitle: LayoutEnumerator
articleTitle: LayoutEnumerator
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Layout.LayoutEnumerator для эффективного перечисления макетов документов. Исследуйте геометрию страницы, текст и структуру без усилий!
type: docs
weight: 3790
url: /ru/net/aspose.words.layout/layoutenumerator/
---
## LayoutEnumerator class

Перечисляет сущности макета страницы документа. Вы можете использовать этот класс для обхода модели макета страницы. Доступные свойства: тип, геометрия, текст и индекс страницы, где отображается сущность, а также общая структура и отношения. Используйте комбинацию[`GetEntity`](../layoutcollector/getentity/) и[`Current`](./current/) перейти к сущности, которая соответствует узлу документа.

Чтобы узнать больше, посетите[Преобразование в формат с фиксированным размером страницы](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) документальная статья.

```csharp
public class LayoutEnumerator
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [LayoutEnumerator](layoutenumerator/)(*[Document](../../aspose.words/document/)*) | Инициализирует новый экземпляр этого класса. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Current](../../aspose.words.layout/layoutenumerator/current/) { get; set; } | Возвращает или задает текущую позицию в модели макета страницы. Это свойство возвращает непрозрачный объект, который соответствует текущей сущности макета. |
| [Document](../../aspose.words.layout/layoutenumerator/document/) { get; } | Получает документ, который этот экземпляр перечисляет. |
| [Item](../../aspose.words.layout/layoutenumerator/item/) { get; } | Получает именованное свойство сущности. |
| [Kind](../../aspose.words.layout/layoutenumerator/kind/) { get; } | Получает тип текущей сущности. Это может быть пустая строка, но никогда`нулевой` . |
| [PageIndex](../../aspose.words.layout/layoutenumerator/pageindex/) { get; } | Возвращает индекс страницы, содержащей текущую сущность, начиная с 1. |
| [Rectangle](../../aspose.words.layout/layoutenumerator/rectangle/) { get; } | Возвращает ограничивающий прямоугольник текущей сущности относительно верхнего левого угла страницы (в точках). |
| [Text](../../aspose.words.layout/layoutenumerator/text/) { get; } | Получает текст текущей сущности span. Выдает для других типов сущностей. |
| [Type](../../aspose.words.layout/layoutenumerator/type/) { get; } | Получает тип текущей сущности. |

## Методы

| Имя | Описание |
| --- | --- |
| [MoveFirstChild](../../aspose.words.layout/layoutenumerator/movefirstchild/)() | Перемещает к первой дочерней сущности. |
| [MoveLastChild](../../aspose.words.layout/layoutenumerator/movelastchild/)() | Перемещает к последнему дочернему объекту. |
| [MoveNext](../../aspose.words.layout/layoutenumerator/movenext/)() | Перемещает к следующему родственному объекту в визуальном порядке. При итерации строк абзаца, разбитого на несколько страниц, этот метод не переместит на следующую страницу, а переместит к следующему объекту на той же странице. |
| [MoveNextLogical](../../aspose.words.layout/layoutenumerator/movenextlogical/)() | Перемещает к следующему родственному объекту в логическом порядке. При итерации строк абзаца, разбитого на несколько страниц, этот метод переместит на следующую строку, даже если она находится на другой странице. |
| [MoveParent](../../aspose.words.layout/layoutenumerator/moveparent/#moveparent)() | Перемещает к родительскому объекту. |
| [MoveParent](../../aspose.words.layout/layoutenumerator/moveparent/#moveparent_1)(*[LayoutEntityType](../layoutentitytype/)*) | Перемещает к родительскому объекту указанного типа. |
| [MovePrevious](../../aspose.words.layout/layoutenumerator/moveprevious/)() | Перемещает к предыдущему родственному объекту. |
| [MovePreviousLogical](../../aspose.words.layout/layoutenumerator/movepreviouslogical/)() | Перемещает к предыдущей одноуровневой сущности в логическом порядке. При итерации строк абзаца, разбитого на несколько страниц, этот метод переместит к предыдущей строке, даже если она находится на другой странице. |
| [Reset](../../aspose.words.layout/layoutenumerator/reset/)() | Перемещает перечислитель на первую страницу документа. |

## Примеры

Показывает способы перемещения по сущностям макета документа.

```csharp
public void LayoutEnumerator()
{
    // Откройте документ, содержащий различные объекты макета.
    // Сущности макета — это страницы, ячейки, строки, линии и другие объекты, включенные в перечисление LayoutEntityType.
    // Каждый объект макета имеет прямоугольное пространство, которое он занимает в теле документа.
    Document doc = new Document(MyDir + "Layout entities.docx");

    // Создать перечислитель, который может обходить эти сущности как дерево.
    LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

    Assert.AreEqual(doc, layoutEnumerator.Document);

    layoutEnumerator.MoveParent(LayoutEntityType.Page);

    Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);
    Assert.Throws<InvalidOperationException>(() => Console.WriteLine(layoutEnumerator.Text));

    // Мы можем вызвать этот метод, чтобы убедиться, что перечислитель будет на первой сущности макета.
    layoutEnumerator.Reset();

    // Существует два порядка, которые определяют, как перечислитель макета продолжает обход сущностей макета
    // когда он сталкивается с сущностями, охватывающими несколько страниц.
    // 1 - В визуальном порядке:
    // При перемещении по дочерним элементам сущности, охватывающим несколько страниц,
    // макет страницы имеет приоритет, и мы переходим к другим дочерним элементам на этой странице и избегаем тех, что на следующей.
    Console.WriteLine("Traversing from first to last, elements between pages separated:");
    TraverseLayoutForward(layoutEnumerator, 1);

    // Наш перечислитель теперь в конце коллекции. Мы можем пройти по сущностям макета назад, чтобы вернуться к началу.
    Console.WriteLine("Traversing from last to first, elements between pages separated:");
    TraverseLayoutBackward(layoutEnumerator, 1);

    // 2 - В логическом порядке:
    // При перемещении по дочерним элементам сущности, охватывающим несколько страниц,
    // перечислитель будет перемещаться между страницами, чтобы обойти все дочерние сущности.
    Console.WriteLine("Traversing from first to last, elements between pages mixed:");
    TraverseLayoutForwardLogical(layoutEnumerator, 1);

    Console.WriteLine("Traversing from last to first, elements between pages mixed:");
    TraverseLayoutBackwardLogical(layoutEnumerator, 1);
}

/// <summary>
/// Перечислить через коллекцию сущностей макета layoutEnumerator спереди назад,
/// в глубинном порядке и в «визуальном» порядке.
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
/// Перечислить через коллекцию сущностей макета layoutEnumerator сзади наперед,
/// в глубинном порядке и в «визуальном» порядке.
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
/// Перечислить через коллекцию сущностей макета layoutEnumerator спереди назад,
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
/// Перечислить через коллекцию сущностей макета layoutEnumerator сзади наперед,
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
/// Вывести информацию о текущей сущности layoutEnumerator на консоль, сделав отступ текста с помощью символов табуляции
/// на основе его глубины относительно корневого узла, который мы предоставили в экземпляре конструктора LayoutEnumerator.
/// Прямоугольник, который мы обрабатываем в конце, представляет собой область и местоположение, которое сущность занимает в документе.
/// </summary>
private static void PrintCurrentEntity(LayoutEnumerator layoutEnumerator, int indent)
{
    string tabs = new string('\t', indent);

    Console.WriteLine(layoutEnumerator.Kind == string.Empty
        ? $"{tabs}-> Entity type: {layoutEnumerator.Type}"
        : $"{tabs}-> Entity type & kind: {layoutEnumerator.Type}, {layoutEnumerator.Kind}");

    // Только интервалы могут содержать текст.
    if (layoutEnumerator.Type == LayoutEntityType.Span)
        Console.WriteLine($"{tabs}   Span contents: \"{layoutEnumerator.Text}\"");

    RectangleF leRect = layoutEnumerator.Rectangle;
    Console.WriteLine($"{tabs}   Rectangle dimensions {leRect.Width}x{leRect.Height}, X={leRect.X} Y={leRect.Y}");
    Console.WriteLine($"{tabs}   Page {layoutEnumerator.PageIndex}");
}
```

### Смотрите также

* пространство имен [Aspose.Words.Layout](../../aspose.words.layout/)
* сборка [Aspose.Words](../../)
