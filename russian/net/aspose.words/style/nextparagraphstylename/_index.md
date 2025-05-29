---
title: Style.NextParagraphStyleName
linktitle: NextParagraphStyleName
articleTitle: NextParagraphStyleName
second_title: Aspose.Words для .NET
description: Узнайте, как эффективно использовать свойство NextParagraphStyleName для автоматизации применения стилей к новым абзацам, улучшая форматирование документа.
type: docs
weight: 140
url: /ru/net/aspose.words/style/nextparagraphstylename/
---
## Style.NextParagraphStyleName property

Возвращает/задает имя стиля, который будет автоматически применен к новому абзацу, вставленному после абзаца a , отформатированного с использованием указанного стиля.

```csharp
public string NextParagraphStyleName { get; set; }
```

## Примечания

Это свойство не используется Aspose.Words. Следующий стиль абзаца будет применен автоматически только при редактировании документа в MS Word.

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
