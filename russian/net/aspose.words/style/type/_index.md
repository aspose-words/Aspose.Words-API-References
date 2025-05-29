---
title: Style.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words для .NET
description: Откройте для себя свойство «Тип стиля», чтобы легко получать доступ к стилям абзацев или символов и настраивать их, улучшая визуальную привлекательность вашего документа.
type: docs
weight: 200
url: /ru/net/aspose.words/style/type/
---
## Style.Type property

Получает тип стиля (абзац или символ).

```csharp
public StyleType Type { get; }
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

* enum [StyleType](../../styletype/)
* class [Style](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
