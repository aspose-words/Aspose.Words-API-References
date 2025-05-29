---
title: StyleCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words для .NET
description: Откройте для себя метод StyleCollection GetEnumerator для легкого перечисления стилей в алфавитном порядке по имени. Повысьте эффективность кодирования сегодня!
type: docs
weight: 90
url: /ru/net/aspose.words/stylecollection/getenumerator/
---
## StyleCollection.GetEnumerator method

Получает объект перечислителя, который будет перечислять стили в алфавитном порядке их имен.

```csharp
public IEnumerator<Style> GetEnumerator()
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

* class [Style](../../style/)
* class [StyleCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
