---
title: ListLabel.LabelValue
linktitle: LabelValue
articleTitle: LabelValue
second_title: Aspose.Words для .NET
description: ListLabel LabelValue свойство. Получает числовое значение для этой метки на С#.
type: docs
weight: 30
url: /ru/net/aspose.words.lists/listlabel/labelvalue/
---
## ListLabel.LabelValue property

Получает числовое значение для этой метки.

```csharp
public int LabelValue { get; }
```

## Примечания

Используйте[`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/) метод для обновления значения этого свойства.

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

* class [ListLabel](../)
* пространство имен [Aspose.Words.Lists](../../../aspose.words.lists/)
* сборка [Aspose.Words](../../../)
