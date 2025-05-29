---
title: LayoutEntityType Enum
linktitle: LayoutEntityType
articleTitle: LayoutEntityType
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Layout.LayoutEntityType, включающее разнообразные типы сущностей макета для улучшенного форматирования документов и бесшовной интеграции.
type: docs
weight: 3780
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
| Page | `1` | Представляет страницу документа. Страница может иметьColumn ,HeaderFooter иComment дочерние сущности. |
| Column | `2` | Представляет столбец текста на странице. Столбец может иметь те же дочерние сущности, что иCell , плюсFootnote ,Endnote иNoteSeparator сущности. |
| Row | `8` | Представляет строку таблицы. Строка может иметьCell как дочерние сущности. |
| Cell | `10` | Представляет ячейку таблицы. Ячейка может иметьLine иRow дочерние сущности. |
| Line | `20` | Представляет строку символов текста и встроенных объектов. Строка может иметьSpan дочерние сущности. |
| Span | `40` | Представляет один или несколько символов в строке. Сюда входят специальные символы, такие как маркеры начала/конца поля, закладки и комментарии. Диапазон не может иметь дочерних сущностей. |
| Footnote | `100` | Представляет собой заполнитель для содержимого сноски. Сноска может иметьNote дочерние сущности. |
| Endnote | `200` | Представляет собой заполнитель для содержимого концевой сноски. Концевая сноска может иметьNote дочерние сущности. |
| Note | `4000` | Представляет собой заполнитель для содержимого заметки. Заметка может иметьLine иRow дочерние сущности. |
| HeaderFooter | `400` | Представляет заполнитель для содержимого верхнего/нижнего колонтитула на странице. HeaderFooter может иметьLine иRow дочерние сущности. |
| TextBox | `800` | Представляет текстовую область внутри фигуры. Текстовое поле может иметьLine иRow дочерние сущности. |
| Comment | `1000` | Представляет собой заполнитель для содержимого комментария. Комментарий может иметьLine иRow дочерние сущности. |
| NoteSeparator | `2000` | Представляет разделитель сносок/концевых сносок. Разделитель примечаний может иметьLine иRow дочерние сущности. |

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
