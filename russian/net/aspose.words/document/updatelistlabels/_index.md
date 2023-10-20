---
title: Document.UpdateListLabels
linktitle: UpdateListLabels
articleTitle: UpdateListLabels
second_title: Aspose.Words для .NET
description: Document UpdateListLabels метод. Обновляет метки списка для всех элементов списка в документе на С#.
type: docs
weight: 760
url: /ru/net/aspose.words/document/updatelistlabels/
---
## Document.UpdateListLabels method

Обновляет метки списка для всех элементов списка в документе.

```csharp
public void UpdateListLabels()
```

## Примечания

Этот метод обновляет свойства метки списка, такие как[`LabelValue`](../../../aspose.words.lists/listlabel/labelvalue/) and [`LabelString`](../../../aspose.words.lists/listlabel/labelstring/) для каждого[`ListLabel`](../../paragraph/listlabel/)объект в документе.

Также этот метод иногда неявно вызывается при обновлении полей в документе. Это требуется , потому что некоторые поля, которые могут ссылаться на номера списка (например, TOC или REF), требуют их актуальности.

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

* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
