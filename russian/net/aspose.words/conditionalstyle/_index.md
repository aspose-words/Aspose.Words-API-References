---
title: ConditionalStyle Class
linktitle: ConditionalStyle
articleTitle: ConditionalStyle
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.ConditionalStyle для расширенного форматирования таблиц. Улучшите свои документы с помощью динамических стилей и улучшите читаемость без усилий.
type: docs
weight: 510
url: /ru/net/aspose.words/conditionalstyle/
---
## ConditionalStyle class

Представляет собой специальное форматирование, применяемое к некоторой области таблицы с назначенным стилем таблицы.

Чтобы узнать больше, посетите[Работа с таблицами](https://docs.aspose.com/words/net/working-with-tables/) документальная статья.

```csharp
public sealed class ConditionalStyle
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Borders](../../aspose.words/conditionalstyle/borders/) { get; } | Получает коллекцию границ ячеек по умолчанию для условного стиля. |
| [BottomPadding](../../aspose.words/conditionalstyle/bottompadding/) { get; set; } | Возвращает или задает размер пространства (в пунктах), добавляемого под содержимым ячеек таблицы. |
| [Font](../../aspose.words/conditionalstyle/font/) { get; } | Получает форматирование символов условного стиля. |
| [LeftPadding](../../aspose.words/conditionalstyle/leftpadding/) { get; set; } | Возвращает или задает размер пространства (в пунктах), добавляемого слева от содержимого ячеек таблицы. |
| [ParagraphFormat](../../aspose.words/conditionalstyle/paragraphformat/) { get; } | Получает форматирование абзаца условного стиля. |
| [RightPadding](../../aspose.words/conditionalstyle/rightpadding/) { get; set; } | Возвращает или задает размер пространства (в пунктах), добавляемого справа от содержимого ячеек таблицы. |
| [Shading](../../aspose.words/conditionalstyle/shading/) { get; } | Получает[`Shading`](../shading/) объект, который ссылается на форматирование штриховки для этого условного стиля. |
| [TopPadding](../../aspose.words/conditionalstyle/toppadding/) { get; set; } | Возвращает или задает размер пространства (в пунктах), добавляемого над содержимым ячеек таблицы. |
| [Type](../../aspose.words/conditionalstyle/type/) { get; } | Получает область таблицы, к которой относится этот условный стиль. |

## Методы

| Имя | Описание |
| --- | --- |
| [ClearFormatting](../../aspose.words/conditionalstyle/clearformatting/)() | Очищает форматирование этого условного стиля. |
| override [Equals](../../aspose.words/conditionalstyle/equals/)(*object*) | Сравнивает этот условный стиль с указанным объектом. |
| override [GetHashCode](../../aspose.words/conditionalstyle/gethashcode/)() | Вычисляет хэш-код для этого объекта. |

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

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
