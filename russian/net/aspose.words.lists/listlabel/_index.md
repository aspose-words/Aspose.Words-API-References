---
title: ListLabel Class
linktitle: ListLabel
articleTitle: ListLabel
second_title: Aspose.Words для .NET
description: Изучите класс Aspose.Words.Lists.ListLabel, чтобы улучшить форматирование документа с помощью настраиваемых свойств меток списков для лучшего контроля и представления.
type: docs
weight: 3940
url: /ru/net/aspose.words.lists/listlabel/
---
## ListLabel class

Определяет свойства, специфичные для метки списка.

Чтобы узнать больше, посетите[Работа со списками](https://docs.aspose.com/words/net/working-with-lists/) документальная статья.

```csharp
public class ListLabel
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Font](../../aspose.words.lists/listlabel/font/) { get; } | Получает шрифт метки списка. |
| [LabelString](../../aspose.words.lists/listlabel/labelstring/) { get; } | Получает строковое представление метки списка. |
| [LabelValue](../../aspose.words.lists/listlabel/labelvalue/) { get; } | Получает числовое значение для этой метки. |

## Примеры

Показывает, как извлечь метки списка всех абзацев, являющихся элементами списка.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
doc.UpdateListLabels();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

// Находим, есть ли у нас список абзацев. В нашем документе наш список использует простые арабские цифры,
// которые начинаются в три и заканчиваются в шесть.
foreach (Paragraph paragraph in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem).ToList())
{
    Console.WriteLine($"List item paragraph #{paras.IndexOf(paragraph)}");

    // Это текст, который мы получаем при выводе этого узла в текстовый формат.
     // Этот текстовый вывод будет опускать списочные метки. Обрезайте любые символы форматирования абзаца.
    string paragraphText = paragraph.ToString(SaveFormat.Text).Trim();
    Console.WriteLine($"\tExported Text: {paragraphText}");

    ListLabel label = paragraph.ListLabel;

    // Это получает позицию абзаца на текущем уровне списка. Если у нас есть список с несколькими уровнями,
    // это скажет нам, в какой позиции он находится на этом уровне.
    Console.WriteLine($"\tNumerical Id: {label.LabelValue}");

    // Объединяем их вместе, чтобы включить метку списка с текстом в вывод.
    Console.WriteLine($"\tList label combined with text: {label.LabelString} {paragraphText}");
}
```

### Смотрите также

* пространство имен [Aspose.Words.Lists](../../aspose.words.lists/)
* сборка [Aspose.Words](../../)
