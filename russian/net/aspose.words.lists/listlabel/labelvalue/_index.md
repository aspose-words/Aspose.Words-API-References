---
title: ListLabel.LabelValue
second_title: Справочник по API Aspose.Words для .NET
description: ListLabel свойство. Получает числовое значение для этой метки.
type: docs
weight: 30
url: /ru/net/aspose.words.lists/listlabel/labelvalue/
---
## ListLabel.LabelValue property

Получает числовое значение для этой метки.

```csharp
public int LabelValue { get; }
```

### Примечания

Используйте[`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/) метод для обновления значения этого свойства.

### Примеры

Показывает, как извлечь метки списка всех абзацев, являющихся элементами списка.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
doc.UpdateListLabels();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

// Определяем, есть ли у нас список абзацев. В нашем документе в нашем списке используются простые арабские цифры,
// которые начинаются с трех и заканчиваются на шести.
foreach (Paragraph paragraph in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem))
{
    Console.WriteLine($"List item paragraph #{paras.IndexOf(paragraph)}");

    // Это текст, который мы получаем при получении, когда мы выводим этот узел в текстовый формат.
    // В этом текстовом выводе метки списка будут пропущены. Обрежьте все символы форматирования абзаца. 
    string paragraphText = paragraph.ToString(SaveFormat.Text).Trim();
    Console.WriteLine($"\tExported Text: {paragraphText}");

    ListLabel label = paragraph.ListLabel;

    // Получаем позицию абзаца на текущем уровне списка. Если у нас есть список с несколькими уровнями,
    // это скажет нам, какая позиция находится на этом уровне.
    Console.WriteLine($"\tNumerical Id: {label.LabelValue}");

    // Объедините их вместе, чтобы включить в вывод метку списка с текстом.
    Console.WriteLine($"\tList label combined with text: {label.LabelString} {paragraphText}");
}
```

### Смотрите также

* class [ListLabel](../)
* пространство имен [Aspose.Words.Lists](../../listlabel/)
* сборка [Aspose.Words](../../../)


