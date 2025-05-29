---
title: Paragraph.JoinRunsWithSameFormatting
linktitle: JoinRunsWithSameFormatting
articleTitle: JoinRunsWithSameFormatting
second_title: Aspose.Words для .NET
description: Легко объединяйте строки с единообразным форматированием в ваших абзацах с помощью метода JoinRunsWithSameFormatting. Улучшите стиль вашего документа сегодня!
type: docs
weight: 300
url: /ru/net/aspose.words/paragraph/joinrunswithsameformatting/
---
## Paragraph.JoinRunsWithSameFormatting method

Объединяет фрагменты с одинаковым форматированием в абзаце.

```csharp
public int JoinRunsWithSameFormatting()
```

### Возвращаемое значение

Количество выполненных соединений. Когда**Н** смежные прогоны объединяются, они считаются**Н - 1** присоединяется.

## Примеры

Показывает, как упростить абзацы путем объединения лишних фрагментов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте четыре фрагмента текста в абзац.
builder.Write("Run 1. ");
builder.Write("Run 2. ");
builder.Write("Run 3. ");
builder.Write("Run 4. ");

// Если мы откроем этот документ в Microsoft Word, абзац будет выглядеть как единый текстовый блок.
// Однако он будет состоять из четырех отдельных фрагментов с одинаковым форматированием. Фрагментированные абзацы, подобные этому
// может возникнуть, когда мы вручную редактируем части одного абзаца много раз в Microsoft Word.
Paragraph para = builder.CurrentParagraph;

Assert.AreEqual(4, para.Runs.Count);

// Измените стиль последнего прогона, чтобы выделить его среди первых трех.
para.Runs[3].Font.StyleIdentifier = StyleIdentifier.Emphasis;

// Мы можем запустить метод «JoinRunsWithSameFormatting» для оптимизации содержимого документа
// путем объединения похожих запусков в один, уменьшая их общее количество.
// Этот метод также возвращает количество запусков, объединенных этим методом.
// Эти два слияния произошли для объединения запусков № 1, № 2 и № 3,
// при этом пропускается запуск №4, поскольку он имеет несовместимый стиль.
Assert.AreEqual(2, para.JoinRunsWithSameFormatting());

// Количество оставшихся запусков будет равно исходному количеству
// минус количество слияний запусков, выполненных методом «JoinRunsWithSameFormatting».
Assert.AreEqual(2, para.Runs.Count);
Assert.AreEqual("Run 1. Run 2. Run 3. ", para.Runs[0].Text);
Assert.AreEqual("Run 4. ", para.Runs[1].Text);
```

### Смотрите также

* class [Paragraph](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
