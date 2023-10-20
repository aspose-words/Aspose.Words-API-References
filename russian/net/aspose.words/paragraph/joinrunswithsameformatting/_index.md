---
title: Paragraph.JoinRunsWithSameFormatting
linktitle: JoinRunsWithSameFormatting
articleTitle: JoinRunsWithSameFormatting
second_title: Aspose.Words для .NET
description: Paragraph JoinRunsWithSameFormatting метод. Объединяет прогоны с тем же форматированием в абзаце на С#.
type: docs
weight: 280
url: /ru/net/aspose.words/paragraph/joinrunswithsameformatting/
---
## Paragraph.JoinRunsWithSameFormatting method

Объединяет прогоны с тем же форматированием в абзаце.

```csharp
public int JoinRunsWithSameFormatting()
```

### Возвращаемое значение

Количество выполненных объединений. Когда**Н** соседние трассы соединяются, они считаются**Н - 1** присоединяется.

## Примеры

Показывает, как упростить абзацы, объединив лишние фрагменты.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем в абзац четыре фрагмента текста.
builder.Write("Run 1. ");
builder.Write("Run 2. ");
builder.Write("Run 3. ");
builder.Write("Run 4. ");

// Если мы откроем этот документ в Microsoft Word, абзац будет выглядеть как одно цельное текстовое тело.
// Однако он будет состоять из четырех отдельных запусков с одинаковым форматированием. Фрагментированные абзацы, подобные этому
// может возникнуть, когда мы много раз вручную редактируем части одного абзаца в Microsoft Word.
Paragraph para = builder.CurrentParagraph;

Assert.AreEqual(4, para.Runs.Count);

// Измените стиль последнего запуска, чтобы выделить его среди первых трех.
para.Runs[3].Font.StyleIdentifier = StyleIdentifier.Emphasis;

// Мы можем запустить метод «JoinRunsWithSameFormatting», чтобы оптимизировать содержимое документа
// путем объединения похожих запусков в один, уменьшая их общее количество.
// Этот метод также возвращает количество запусков, объединенных этим методом.
// Эти два слияния произошли для объединения запусков №1, №2 и №3,
// оставляя прогон #4, поскольку он имеет несовместимый стиль.
Assert.AreEqual(2, para.JoinRunsWithSameFormatting());

// Количество оставшихся запусков будет равно исходному счетчику
// минус количество слияний, выполненных методом "JoinRunsWithSameFormatting".
Assert.AreEqual(2, para.Runs.Count);
Assert.AreEqual("Run 1. Run 2. Run 3. ", para.Runs[0].Text);
Assert.AreEqual("Run 4. ", para.Runs[1].Text);
```

### Смотрите также

* class [Paragraph](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
