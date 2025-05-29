---
title: Document.UpdateListLabels
linktitle: UpdateListLabels
articleTitle: UpdateListLabels
second_title: Aspose.Words для .NET
description: С легкостью обновляйте все метки элементов списка в документе с помощью метода UpdateListLabels, обеспечивая согласованность и ясность вашего контента.
type: docs
weight: 820
url: /ru/net/aspose.words/document/updatelistlabels/
---
## Document.UpdateListLabels method

Обновляет метки списка для всех элементов списка в документе.

```csharp
public void UpdateListLabels()
```

## Примечания

Этот метод обновляет свойства метки списка, такие как[`LabelValue`](../../../aspose.words.lists/listlabel/labelvalue/) и [`LabelString`](../../../aspose.words.lists/listlabel/labelstring/) для каждого[`ListLabel`](../../paragraph/listlabel/) объект в документе.

Также этот метод иногда неявно вызывается при обновлении полей в документе. Это required , поскольку некоторые поля, которые могут ссылаться на номера списков (например, TOC или REF), требуют их обновления.

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

* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
