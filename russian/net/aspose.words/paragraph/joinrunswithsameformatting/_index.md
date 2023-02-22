---
title: Paragraph.JoinRunsWithSameFormatting
second_title: Справочник по API Aspose.Words для .NET
description: Paragraph метод. Объединяет прогоны с тем же форматированием что и абзац.
type: docs
weight: 280
url: /ru/net/aspose.words/paragraph/joinrunswithsameformatting/
---
## Paragraph.JoinRunsWithSameFormatting method

Объединяет прогоны с тем же форматированием, что и абзац.

```csharp
public int JoinRunsWithSameFormatting()
```

### Возвращаемое значение

Количество выполненных объединений. Когда **Н** соединяются соседние прогоны, они считаются **Н - 1** присоединяется.

### Примеры

Показывает, как упростить абзацы, объединив лишние строки.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем четыре строки текста в абзац.
builder.Write("Run 1. ");
builder.Write("Run 2. ");
builder.Write("Run 3. ");
builder.Write("Run 4. ");

// Если мы откроем этот документ в Microsoft Word, абзац будет выглядеть как одно сплошное текстовое тело.
// Однако он будет состоять из четырех отдельных прогонов с одинаковым форматированием. Такие фрагментированные абзацы
// может возникнуть, когда мы много раз вручную редактируем части одного абзаца в Microsoft Word.
Paragraph para = builder.CurrentParagraph;

Assert.AreEqual(4, para.Runs.Count);

// Измените стиль последнего запуска, чтобы он отличался от первых трех.
para.Runs[3].Font.StyleIdentifier = StyleIdentifier.Emphasis;

// Мы можем запустить метод "JoinRunsWithSameFormatting" для оптимизации содержимого документа
// объединяя похожие прогоны в один, уменьшая их общее количество.
// Этот метод также возвращает количество прогонов, объединенных этим методом.
// Эти два слияния произошли для объединения прогонов №1, №2 и №3,
// при этом пропускаем Run #4, потому что он имеет несовместимый стиль.
Assert.AreEqual(2, para.JoinRunsWithSameFormatting());

// Количество оставшихся прогонов будет равно исходному количеству
// минус количество слияний прогонов, выполненных методом "JoinRunsWithSameFormatting".
Assert.AreEqual(2, para.Runs.Count);
Assert.AreEqual("Run 1. Run 2. Run 3. ", para.Runs[0].Text);
Assert.AreEqual("Run 4. ", para.Runs[1].Text);
```

### Смотрите также

* class [Paragraph](../)
* пространство имен [Aspose.Words](../../paragraph/)
* сборка [Aspose.Words](../../../)


