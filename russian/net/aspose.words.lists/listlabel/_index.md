---
title: ListLabel Class
linktitle: ListLabel
articleTitle: ListLabel
second_title: Aspose.Words для .NET
description: Aspose.Words.Lists.ListLabel сорт. Определяет свойства специфичные для метки списка на С#.
type: docs
weight: 3490
url: /ru/net/aspose.words.lists/listlabel/
---
## ListLabel class

Определяет свойства, специфичные для метки списка.

Чтобы узнать больше, посетите[Работа со списками](https://docs.aspose.com/words/net/working-with-lists/) статья документации.

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

Показывает, как извлечь метки списка всех абзацев, которые являются элементами списка.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
doc.UpdateListLabels();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

// Проверяем, есть ли у нас список абзацев. В нашем документе в списке используются простые арабские цифры,
// которые начинаются в три и заканчиваются в шесть.
foreach (Paragraph paragraph in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem))
{
    Console.WriteLine($"List item paragraph #{paras.IndexOf(paragraph)}");

    // Это текст, который мы получаем при выводе этого узла в текстовый формат.
     // В этом текстовом выводе метки списков будут пропущены. Обрежьте любые символы форматирования абзаца.
    string paragraphText = paragraph.ToString(SaveFormat.Text).Trim();
    Console.WriteLine($"\tExported Text: {paragraphText}");

    ListLabel label = paragraph.ListLabel;

    // Получает позицию абзаца на текущем уровне списка. Если у нас есть список с несколькими уровнями,
    // это скажет нам, в какой позиции он находится на этом уровне.
    Console.WriteLine($"\tNumerical Id: {label.LabelValue}");

    // Объедините их вместе, чтобы включить метку списка в текст вывода.
    Console.WriteLine($"\tList label combined with text: {label.LabelString} {paragraphText}");
}
```

### Смотрите также

* пространство имен [Aspose.Words.Lists](../../aspose.words.lists/)
* сборка [Aspose.Words](../../)
