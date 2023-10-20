---
title: TextColumnCollection Class
linktitle: TextColumnCollection
articleTitle: TextColumnCollection
second_title: Aspose.Words для .NET
description: Aspose.Words.TextColumnCollection сорт. КоллекцияTextColumn объекты которые представляют все столбцы текста в разделе документа на С#.
type: docs
weight: 6400
url: /ru/net/aspose.words/textcolumncollection/
---
## TextColumnCollection class

Коллекция[`TextColumn`](../textcolumn/) объекты, которые представляют все столбцы текста в разделе документа.

Чтобы узнать больше, посетите[Работа с разделами](https://docs.aspose.com/words/net/working-with-sections/) статья документации.

```csharp
public class TextColumnCollection
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words/textcolumncollection/count/) { get; } | Получает количество столбцов в разделе документа. |
| [EvenlySpaced](../../aspose.words/textcolumncollection/evenlyspaced/) { get; set; } | Истинно, если текстовые столбцы имеют одинаковую ширину и расположены на равном расстоянии. |
| [Item](../../aspose.words/textcolumncollection/item/) { get; } | Возвращает текстовый столбец по указанному индексу. |
| [LineBetween](../../aspose.words/textcolumncollection/linebetween/) { get; set; } | Когда`истинный` добавляет вертикальную линию между столбцами. |
| [Spacing](../../aspose.words/textcolumncollection/spacing/) { get; set; } | Если столбцы расположены равномерно, получает или задает расстояние между каждым столбцом в пунктах. |
| [Width](../../aspose.words/textcolumncollection/width/) { get; } | Если столбцы расположены на равном расстоянии друг от друга, получает ширину столбцов. |

## Методы

| Имя | Описание |
| --- | --- |
| [SetCount](../../aspose.words/textcolumncollection/setcount/)(*int*) | Упорядочивает текст в указанное количество текстовых столбцов. |

## Примечания

Использовать[`SetCount`](./setcount/) чтобы установить количество текстовых столбцов.

Чтобы сделать все столбцы одинаковой ширины и равномерно расположенными, установите[`EvenlySpaced`](./evenlyspaced/) к`истинный` и укажите расстояние между столбцами в[`Spacing`](./spacing/). MS Word will автоматически рассчитывает ширину столбцов.

Если у вас есть[`EvenlySpaced`](./evenlyspaced/) установлен в`ЛОЖЬ` , вам необходимо указать ширину и интервал для каждого столбца индивидуально. Используйте индексатор для доступа к отдельным[`TextColumn`](../textcolumn/) объекты.

При использовании произвольной ширины столбцов убедитесь, что сумма ширин всех столбцов и интервалов между ними равна ширине страницы за вычетом левого и правого полей страницы.

## Примеры

Показывает, как создать в разделе несколько равномерно расположенных столбцов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.Spacing = 100;
columns.SetCount(2);

builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");

doc.Save(ArtifactsDir + "PageSetup.ColumnsSameWidth.docx");
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
