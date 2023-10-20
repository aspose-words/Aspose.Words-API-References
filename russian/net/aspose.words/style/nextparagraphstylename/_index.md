---
title: Style.NextParagraphStyleName
linktitle: NextParagraphStyleName
articleTitle: NextParagraphStyleName
second_title: Aspose.Words для .NET
description: Style NextParagraphStyleName свойство. Получает/устанавливает имя стиля который будет автоматически применяться к новому абзацу вставленному после абзаца a  отформатированного с использованием указанного стиля на С#.
type: docs
weight: 130
url: /ru/net/aspose.words/style/nextparagraphstylename/
---
## Style.NextParagraphStyleName property

Получает/устанавливает имя стиля, который будет автоматически применяться к новому абзацу, вставленному после абзаца a , отформатированного с использованием указанного стиля.

```csharp
public string NextParagraphStyleName { get; set; }
```

## Примечания

Это свойство не используется Aspose.Words. Следующий стиль абзаца only будет применен автоматически при редактировании документа в MS Word.

## Примеры

Показывает, как получить доступ к коллекции стилей документа.

```csharp
Document doc = new Document();

Assert.AreEqual(4, doc.Styles.Count);

// Перечисляем и перечисляем все стили, которые по умолчанию содержит документ, созданный с помощью Aspose.Words.
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
