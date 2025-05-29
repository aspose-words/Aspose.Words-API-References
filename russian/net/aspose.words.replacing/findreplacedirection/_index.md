---
title: FindReplaceDirection Enum
linktitle: FindReplaceDirection
articleTitle: FindReplaceDirection
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words FindReplaceDirection для эффективной замены текста. Оптимизируйте обработку документов с точным контролем направления.
type: docs
weight: 5340
url: /ru/net/aspose.words.replacing/findreplacedirection/
---
## FindReplaceDirection enumeration

Указывает направление для операций замены.

```csharp
public enum FindReplaceDirection
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Forward | `0` | Совпадающие элементы заменяются от первого к последнему. |
| Backward | `1` | Совпадающие элементы заменяются с последнего на первый. |

## Примеры

Показывает, как определить, в каком направлении операция поиска и замены проходит по документу.

```csharp
public void Direction(FindReplaceDirection findReplaceDirection)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Вставляем три записи, которые можно искать с помощью шаблона регулярного выражения.
    // Поместите один из этих фрагментов в текстовое поле.
    builder.Writeln("Match 1.");
    builder.Writeln("Match 2.");
    builder.Writeln("Match 3.");
    builder.Writeln("Match 4.");

    // Мы можем использовать объект «FindReplaceOptions» для изменения процесса поиска и замены.
    FindReplaceOptions options = new FindReplaceOptions();

    // Назначаем пользовательский обратный вызов свойству "ReplacingCallback".
    TextReplacementRecorder callback = new TextReplacementRecorder();
    options.ReplacingCallback = callback;

    // Установите свойство "Direction" на "FindReplaceDirection.Backward", чтобы получить функцию поиска и замены
    // операция начинается с конца диапазона и возвращается к началу.
    // Установите свойство "Direction" на "FindReplaceDirection.Forward", чтобы получить функцию поиска и замены
    // операция начинается с начала диапазона и продолжается до конца.
    options.Direction = findReplaceDirection;

    doc.Range.Replace(new Regex(@"Match \d*"), "Replacement", options);

    Assert.AreEqual("Replacement.\r" +
                    "Replacement.\r" +
                    "Replacement.\r" +
                    "Replacement.", doc.GetText().Trim());

    switch (findReplaceDirection)
    {
        case FindReplaceDirection.Forward:
            Assert.AreEqual(new[] { "Match 1", "Match 2", "Match 3", "Match 4" }, callback.Matches);
            break;
        case FindReplaceDirection.Backward:
            Assert.AreEqual(new[] { "Match 4", "Match 3", "Match 2", "Match 1" }, callback.Matches);
            break;
    }
}

/// <summary>
/// Записывает все совпадения, которые встречаются во время операции поиска и замены, в том порядке, в котором они происходят.
/// </summary>
private class TextReplacementRecorder : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs e)
    {
        Matches.Add(e.Match.Value);
        return ReplaceAction.Replace;
    }

    public List<string> Matches { get; } = new List<string>();
}
```

### Смотрите также

* пространство имен [Aspose.Words.Replacing](../../aspose.words.replacing/)
* сборка [Aspose.Words](../../)
