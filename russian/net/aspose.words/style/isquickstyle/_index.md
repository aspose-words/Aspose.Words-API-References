---
title: Style.IsQuickStyle
linktitle: IsQuickStyle
articleTitle: IsQuickStyle
second_title: Aspose.Words для .NET
description: Узнайте, как свойство IsQuickStyle расширяет возможности MS Word, отображая стили в галерее быстрых стилей для легкого доступа и улучшения рабочего процесса.
type: docs
weight: 80
url: /ru/net/aspose.words/style/isquickstyle/
---
## Style.IsQuickStyle property

Указывает, отображается ли этот стиль в галерее быстрых стилей в пользовательском интерфейсе MS Word.

```csharp
public bool IsQuickStyle { get; set; }
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

* class [Style](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
