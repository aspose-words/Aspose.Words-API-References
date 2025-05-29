---
title: TextColumnCollection Class
linktitle: TextColumnCollection
articleTitle: TextColumnCollection
second_title: Aspose.Words для .NET
description: Исследуйте Aspose.Words.TextColumnCollection, чтобы легко управлять текстовыми столбцами в ваших документах. Улучшите форматирование ваших документов с легкостью!
type: docs
weight: 7250
url: /ru/net/aspose.words/textcolumncollection/
---
## TextColumnCollection class

Коллекция[`TextColumn`](../textcolumn/) объекты, представляющие все столбцы текста в разделе документа.

Чтобы узнать больше, посетите[Работа с разделами](https://docs.aspose.com/words/net/working-with-sections/) документальная статья.

```csharp
public class TextColumnCollection
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words/textcolumncollection/count/) { get; } | Получает количество столбцов в разделе документа. |
| [EvenlySpaced](../../aspose.words/textcolumncollection/evenlyspaced/) { get; set; } | Истина, если текстовые столбцы имеют одинаковую ширину и равномерно распределены. |
| [Item](../../aspose.words/textcolumncollection/item/) { get; } | Возвращает текстовый столбец по указанному индексу. |
| [LineBetween](../../aspose.words/textcolumncollection/linebetween/) { get; set; } | Когда`истинный` , добавляет вертикальную линию между столбцами. |
| [Spacing](../../aspose.words/textcolumncollection/spacing/) { get; set; } | Когда столбцы расположены равномерно, возвращает или задает величину пространства между каждым столбцом в пунктах. |
| [Width](../../aspose.words/textcolumncollection/width/) { get; } | Когда столбцы расположены равномерно, получает ширину столбцов. |

## Методы

| Имя | Описание |
| --- | --- |
| [SetCount](../../aspose.words/textcolumncollection/setcount/)(*int*) | Располагает текст в указанном количестве текстовых столбцов. |

## Примечания

Использовать[`SetCount`](./setcount/) для установки количества текстовых столбцов.

Чтобы сделать все столбцы одинаковой ширины и равномерно распределенными, установите[`EvenlySpaced`](./evenlyspaced/) к`истинный` и укажите расстояние между столбцами в[`Spacing`](./spacing/). MS Word автоматически рассчитает ширину столбцов.

Если у вас есть[`EvenlySpaced`](./evenlyspaced/) установлен на`ЛОЖЬ` , вам необходимо указать ширину и интервал для каждого столбца x000d_ по отдельности. Используйте индексатор для доступа к отдельным[`TextColumn`](../textcolumn/) объекты.

При использовании нестандартной ширины столбцов убедитесь, что сумма ширины всех столбцов и интервалов между ними равна ширине страницы за вычетом левого и правого полей страницы.

## Примеры

Показывает, как создать несколько равномерно распределенных столбцов в разделе.

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
