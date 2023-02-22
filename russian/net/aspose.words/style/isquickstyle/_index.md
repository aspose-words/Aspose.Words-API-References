---
title: Style.IsQuickStyle
second_title: Справочник по API Aspose.Words для .NET
description: Style свойство. Указывает отображается ли этот стиль в галерее экспрессстилей в пользовательском интерфейсе MS Word.
type: docs
weight: 70
url: /ru/net/aspose.words/style/isquickstyle/
---
## Style.IsQuickStyle property

Указывает, отображается ли этот стиль в галерее экспресс-стилей в пользовательском интерфейсе MS Word.

```csharp
public bool IsQuickStyle { get; set; }
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

* class [Style](../)
* пространство имен [Aspose.Words](../../style/)
* сборка [Aspose.Words](../../../)


