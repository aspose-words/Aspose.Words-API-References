---
title: LayoutEnumerator Class
linktitle: LayoutEnumerator
articleTitle: LayoutEnumerator
second_title: Aspose.Words для .NET
description: Aspose.Words.Layout.LayoutEnumerator сорт. Перечисляет объекты макета страницы документа. Этот класс можно использовать для обхода модели макета страницы. Доступными свойствами являются тип геометрия текст и индекс страницы на которой отображается объект  а также общая структура и связи. Используйте комбинациюGetEntity иCurrent перейти к объекту который соответствует узлу документа на С#.
type: docs
weight: 3340
url: /ru/net/aspose.words.layout/layoutenumerator/
---
## LayoutEnumerator class

Перечисляет объекты макета страницы документа. Этот класс можно использовать для обхода модели макета страницы. Доступными свойствами являются тип, геометрия, текст и индекс страницы, на которой отображается объект, , а также общая структура и связи. Используйте комбинацию[`GetEntity`](../layoutcollector/getentity/) и[`Current`](./current/) перейти к объекту, который соответствует узлу документа.

Чтобы узнать больше, посетите[Преобразование в формат фиксированной страницы](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) статья документации.

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
| [Current](../../aspose.words.layout/layoutenumerator/current/) { get; set; } | Получает или задает текущую позицию в модели макета страницы. Это свойство возвращает непрозрачный объект, соответствующий текущему объекту макета. |
| [Document](../../aspose.words.layout/layoutenumerator/document/) { get; } | Получает документ, который перечисляет этот экземпляр. |
| [Item](../../aspose.words.layout/layoutenumerator/item/) { get; } | Получает именованное свойство объекта. |
| [Kind](../../aspose.words.layout/layoutenumerator/kind/) { get; } | Получает тип текущего объекта. Это может быть пустая строка, но никогда`нулевой` . |
| [PageIndex](../../aspose.words.layout/layoutenumerator/pageindex/) { get; } | Получает индекс страницы, отсчитываемый от 1, которая содержит текущий объект. |
| [Rectangle](../../aspose.words.layout/layoutenumerator/rectangle/) { get; } | Возвращает ограничивающий прямоугольник текущего объекта относительно верхнего левого угла страницы (в пунктах). |
| [Text](../../aspose.words.layout/layoutenumerator/text/) { get; } | Получает текст текущего объекта диапазона. Выдает для других типов объектов. |
| [Type](../../aspose.words.layout/layoutenumerator/type/) { get; } | Получает тип текущего объекта. |

## Методы

| Имя | Описание |
| --- | --- |
| [MoveFirstChild](../../aspose.words.layout/layoutenumerator/movefirstchild/)() | Переходит к первому дочернему объекту. |
| [MoveLastChild](../../aspose.words.layout/layoutenumerator/movelastchild/)() | Переход к последнему дочернему объекту. |
| [MoveNext](../../aspose.words.layout/layoutenumerator/movenext/)() | Переходит к следующему одноуровневому объекту в визуальном порядке. При повторении строк абзаца, разбитого на страницы, этот метод не перемещается на следующую страницу, а скорее переходит к следующему объекту на той же странице. |
| [MoveNextLogical](../../aspose.words.layout/layoutenumerator/movenextlogical/)() | Переходит к следующему одноуровневому объекту в логическом порядке. При повторении строк абзаца, разбитого на страницы, этот метод перейдет к следующей строке, даже если он находится на другой странице. |
| [MoveParent](../../aspose.words.layout/layoutenumerator/moveparent/#moveparent)() | Перемещается к родительскому объекту. |
| [MoveParent](../../aspose.words.layout/layoutenumerator/moveparent/#moveparent_1)(*[LayoutEntityType](../layoutentitytype/)*) | Перемещается к родительскому объекту указанного типа. |
| [MovePrevious](../../aspose.words.layout/layoutenumerator/moveprevious/)() | Переход к предыдущему родственному объекту. |
| [MovePreviousLogical](../../aspose.words.layout/layoutenumerator/movepreviouslogical/)() | Переходит к предыдущему одноуровневому объекту в логическом порядке. При повторении строк абзаца, разбитого на страницы, этот метод переместится на предыдущую строку, даже если она находится на другой странице. |
| [Reset](../../aspose.words.layout/layoutenumerator/reset/)() | Перемещает перечислитель на первую страницу документа. |

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

* пространство имен [Aspose.Words.Layout](../../aspose.words.layout/)
* сборка [Aspose.Words](../../)
