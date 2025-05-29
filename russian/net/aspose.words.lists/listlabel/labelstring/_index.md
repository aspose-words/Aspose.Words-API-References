---
title: ListLabel.LabelString
linktitle: LabelString
articleTitle: LabelString
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ListLabel LabelString для простого строкового представления меток списков, что позволит без труда улучшить представление и организацию данных.
type: docs
weight: 20
url: /ru/net/aspose.words.lists/listlabel/labelstring/
---
## ListLabel.LabelString property

Получает строковое представление метки списка.

```csharp
public string LabelString { get; }
```

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

* class [ListLabel](../)
* пространство имен [Aspose.Words.Lists](../../../aspose.words.lists/)
* сборка [Aspose.Words](../../../)
