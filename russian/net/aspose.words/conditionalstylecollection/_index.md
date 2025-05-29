---
title: ConditionalStyleCollection Class
linktitle: ConditionalStyleCollection
articleTitle: ConditionalStyleCollection
second_title: Aspose.Words для .NET
description: Изучите класс Aspose.Words.ConditionalStyleCollection для эффективного управления объектами ConditionalStyle, улучшения форматирования и настройки документов.
type: docs
weight: 520
url: /ru/net/aspose.words/conditionalstylecollection/
---
## ConditionalStyleCollection class

Представляет собой коллекцию[`ConditionalStyle`](../conditionalstyle/) объекты.

Чтобы узнать больше, посетите[Работа с таблицами](https://docs.aspose.com/words/net/working-with-tables/) документальная статья.

```csharp
public sealed class ConditionalStyleCollection : IEnumerable<ConditionalStyle>
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [BottomLeftCell](../../aspose.words/conditionalstylecollection/bottomleftcell/) { get; } | Получает стиль нижней левой ячейки. |
| [BottomRightCell](../../aspose.words/conditionalstylecollection/bottomrightcell/) { get; } | Получает стиль нижней правой ячейки. |
| [Count](../../aspose.words/conditionalstylecollection/count/) { get; } | Получает количество условных стилей в коллекции. |
| [EvenColumnBanding](../../aspose.words/conditionalstylecollection/evencolumnbanding/) { get; } | Получает стиль полос четных столбцов. |
| [EvenRowBanding](../../aspose.words/conditionalstylecollection/evenrowbanding/) { get; } | Получает стиль полос четных строк. |
| [FirstColumn](../../aspose.words/conditionalstylecollection/firstcolumn/) { get; } | Получает стиль первого столбца. |
| [FirstRow](../../aspose.words/conditionalstylecollection/firstrow/) { get; } | Получает стиль первой строки. |
| [Item](../../aspose.words/conditionalstylecollection/item/) { get; } | Извлекает[`ConditionalStyle`](../conditionalstyle/) объект по условному стилю type. (2 indexers) |
| [LastColumn](../../aspose.words/conditionalstylecollection/lastcolumn/) { get; } | Получает последний стиль столбца. |
| [LastRow](../../aspose.words/conditionalstylecollection/lastrow/) { get; } | Получает стиль последней строки. |
| [OddColumnBanding](../../aspose.words/conditionalstylecollection/oddcolumnbanding/) { get; } | Получает стиль полос нечетных столбцов. |
| [OddRowBanding](../../aspose.words/conditionalstylecollection/oddrowbanding/) { get; } | Получает стиль чередования нечетных строк. |
| [TopLeftCell](../../aspose.words/conditionalstylecollection/topleftcell/) { get; } | Получает стиль верхней левой ячейки. |
| [TopRightCell](../../aspose.words/conditionalstylecollection/toprightcell/) { get; } | Получает стиль верхней правой ячейки. |

## Методы

| Имя | Описание |
| --- | --- |
| [ClearFormatting](../../aspose.words/conditionalstylecollection/clearformatting/)() | Очищает все условные стили таблицы style. |
| [GetEnumerator](../../aspose.words/conditionalstylecollection/getenumerator/)() | Возвращает объект перечислителя, который можно использовать для перебора всех условных стилей в коллекции. |

## Примечания

Невозможно добавлять или удалять элементы из этой коллекции. Она содержит постоянный набор элементов: один элемент для каждого значения[`ConditionalStyleType`](../conditionalstyletype/) тип перечисления.

## Примеры

Показывает, как работать с определенными стилями областей таблицы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell 1");
builder.InsertCell();
builder.Write("Cell 2");
builder.EndRow();
builder.InsertCell();
builder.Write("Cell 3");
builder.InsertCell();
builder.Write("Cell 4");
builder.EndTable();

// Создать собственный стиль таблицы.
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");

// Условные стили — это изменения форматирования, которые затрагивают только некоторые ячейки таблицы.
// на основе предиката, например, нахождения ячеек в последней строке.
// Ниже приведены три способа доступа к условным стилям стиля таблицы из коллекции «ConditionalStyles».
// 1 - По типу стиля:
tableStyle.ConditionalStyles[ConditionalStyleType.FirstRow].Shading.BackgroundPatternColor = Color.AliceBlue;

// 2 - По индексу:
tableStyle.ConditionalStyles[0].Borders.Color = Color.Black;
tableStyle.ConditionalStyles[0].Borders.LineStyle = LineStyle.DotDash;
Assert.AreEqual(ConditionalStyleType.FirstRow, tableStyle.ConditionalStyles[0].Type);

// 3 - Как свойство:
tableStyle.ConditionalStyles.FirstRow.ParagraphFormat.Alignment = ParagraphAlignment.Center;

// Применить отступы и форматирование текста к условным стилям.
tableStyle.ConditionalStyles.LastRow.BottomPadding = 10;
tableStyle.ConditionalStyles.LastRow.LeftPadding = 10;
tableStyle.ConditionalStyles.LastRow.RightPadding = 10;
tableStyle.ConditionalStyles.LastRow.TopPadding = 10;
tableStyle.ConditionalStyles.LastColumn.Font.Bold = true;

// Перечислить все возможные условия стиля.
using (IEnumerator<ConditionalStyle> enumerator = tableStyle.ConditionalStyles.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        ConditionalStyle currentStyle = enumerator.Current;
        if (currentStyle != null) Console.WriteLine(currentStyle.Type);
    }
}

// Применяем к таблице пользовательский стиль, содержащий все условные стили.
table.Style = tableStyle;

// Наш стиль применяет некоторые условные стили по умолчанию.
Assert.AreEqual(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands, 
    table.StyleOptions);

// Все остальные стили нам нужно будет включить самостоятельно через свойство «StyleOptions».
table.StyleOptions = table.StyleOptions | TableStyleOptions.LastRow | TableStyleOptions.LastColumn;

doc.Save(ArtifactsDir + "Table.ConditionalStyles.docx");
```

### Смотрите также

* class [ConditionalStyle](../conditionalstyle/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
