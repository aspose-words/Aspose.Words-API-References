---
title: Style.Type
second_title: Справочник по API Aspose.Words для .NET
description: Style свойство. Получает тип стиля абзац или символ.
type: docs
weight: 160
url: /ru/net/aspose.words/style/type/
---
## Style.Type property

Получает тип стиля (абзац или символ).

```csharp
public StyleType Type { get; }
```

### Примеры

Показывает, как получить доступ к коллекции стилей документа.

```csharp
Document doc = new Document();

Assert.AreEqual(4, doc.Styles.Count);

// Перечислить и перечислить все стили, которые документ, созданный с помощью Aspose.Words, содержит по умолчанию.
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
* пространство имен [Aspose.Words](../../style/)
* сборка [Aspose.Words](../../../)


