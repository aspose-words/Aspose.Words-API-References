---
title: LayoutEntityType Enum
linktitle: LayoutEntityType
articleTitle: LayoutEntityType
second_title: Aspose.Words для .NET
description: Aspose.Words.Layout.LayoutEntityType перечисление. Типы объектов макета на С#.
type: docs
weight: 3330
url: /ru/net/aspose.words.layout/layoutentitytype/
---
## LayoutEntityType enumeration

Типы объектов макета.

```csharp
[Flags]
public enum LayoutEntityType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Значение по умолчанию. |
| Page | `1` | Представляет страницу документа. Страница может иметьColumn ,HeaderFooter иComment дочерние объекты. |
| Column | `2` | Представляет столбец текста на странице. Столбец может иметь те же дочерние объекты, что иCell , плюсFootnote ,Endnote иNoteSeparator сущности. |
| Row | `8` | Представляет строку таблицы. Строка может иметьCell как дочерние объекты. |
| Cell | `10` | Представляет ячейку таблицы. Ячейка может иметьLine иRow дочерние объекты. |
| Line | `20` | Представляет строку символов текста и встроенных объектов. Строка может иметьSpan дочерние объекты. |
| Span | `40` | Представляет один или несколько символов в строке. Сюда входят специальные символы, такие как маркеры начала/конца поля, закладки и комментарии. Span не может иметь дочерних объектов. |
| Footnote | `100` | Представляет заполнитель для содержимого сноски. Сноска может иметьNote дочерние объекты. |
| Endnote | `200` | Представляет заполнитель для содержимого концевой сноски. Конечная сноска может иметьNote дочерние объекты. |
| Note | `4000` | Представляет заполнитель для содержимого примечания. Примечание может иметьLine иRow дочерние объекты. |
| HeaderFooter | `400` | Представляет заполнитель для содержимого верхнего и нижнего колонтитула на странице. HeaderFooter может иметьLine иRow дочерние объекты. |
| TextBox | `800` | Представляет текстовую область внутри фигуры. Текстовое поле может иметьLine иRow дочерние объекты. |
| Comment | `1000` | Представляет заполнитель для содержимого комментария. Комментарий может иметьLine иRow дочерние объекты. |
| NoteSeparator | `2000` | Представляет разделитель сносок/концевых сносок. NoteSeparator может иметьLine иRow дочерние объекты. |

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
