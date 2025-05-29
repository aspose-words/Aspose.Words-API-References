---
title: StyleCollection.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words для .NET
description: Получите доступ к документу владельца без усилий с помощью StyleCollection. Откройте для себя бесперебойное управление документами и улучшите свой рабочий процесс сегодня!
type: docs
weight: 40
url: /ru/net/aspose.words/stylecollection/document/
---
## StyleCollection.Document property

Получает документ владельца.

```csharp
public DocumentBase Document { get; }
```

## Примеры

Показывает, как получить доступ к коллекции стилей документа.

```csharp
Document doc = new Document();

Assert.AreEqual(4, doc.Styles.Count);

// Перечислить и вывести список всех стилей, которые по умолчанию содержит документ, созданный с помощью Aspose.Words.
using (IEnumerator<Style> stylesEnum = doc.Styles.GetEnumerator())
{
    while (stylesEnum.MoveNext())
    {
        Style curStyle = stylesEnum.Current;
        Console.WriteLine($"Style name:\t\"{curStyle.Name}\", of type \"{curStyle.Type}\"");
        Console.WriteLine($"\tSubsequent style:\t{curStyle.NextParagraphStyleName}");
        Console.WriteLine($"\tIs heading:\t\t\t{curStyle.IsHeading}");
        Console.WriteLine($"\tIs QuickStyle:\t\t{curStyle.IsQuickStyle}");

        Assert.AreEqual(doc, curStyle.Document);
    }
}
```

### Смотрите также

* class [DocumentBase](../../documentbase/)
* class [StyleCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
