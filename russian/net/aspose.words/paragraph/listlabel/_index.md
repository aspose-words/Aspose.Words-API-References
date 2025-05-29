---
title: Paragraph.ListLabel
linktitle: ListLabel
articleTitle: ListLabel
second_title: Aspose.Words для .NET
description: Доступ и форматирование нумерации списка с помощью свойства Paragraph ListLabel. Улучшите организацию и ясность вашего документа без усилий!
type: docs
weight: 160
url: /ru/net/aspose.words/paragraph/listlabel/
---
## Paragraph.ListLabel property

Получает`ListLabel`объект, который обеспечивает доступ к значению нумерации списка и форматированию для этого абзаца.

```csharp
public ListLabel ListLabel { get; }
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

* class [ListLabel](../../../aspose.words.lists/listlabel/)
* class [Paragraph](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
