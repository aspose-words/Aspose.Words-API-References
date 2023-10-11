---
title: FindReplaceOptions.Direction
second_title: Справочник по API Aspose.Words для .NET
description: FindReplaceOptions свойство. Выбирает направление замены. Значение по умолчаниюForward .
type: docs
weight: 40
url: /ru/net/aspose.words.replacing/findreplaceoptions/direction/
---
## FindReplaceOptions.Direction property

Выбирает направление замены. Значение по умолчанию:Forward .

```csharp
public FindReplaceDirection Direction { get; set; }
```

### Примеры

Показывает, как определить, в каком направлении проходит операция поиска и замены по документу.

```csharp
public void Direction(FindReplaceDirection findReplaceDirection)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Вставляем три прогона, которые мы можем найти, используя шаблон регулярного выражения.
    // Поместите один из этих запусков в текстовое поле.
    builder.Writeln("Match 1.");
    builder.Writeln("Match 2.");
    builder.Writeln("Match 3.");
    builder.Writeln("Match 4.");

    // Мы можем использовать объект «FindReplaceOptions» для изменения процесса поиска и замены.
    FindReplaceOptions options = new FindReplaceOptions();

    // Назначаем собственный обратный вызов свойству «ReplacingCallback».
    TextReplacementRecorder callback = new TextReplacementRecorder();
    options.ReplacingCallback = callback;

    // Установите для свойства Direction значение FindReplaceDirection.Backward, чтобы получить функцию поиска и замены.
    // операция, которая начинается с конца диапазона и возвращается к началу.
    // Установите для свойства Direction значение FindReplaceDirection.Backward, чтобы получить функцию поиска и замены.
    // операция, которая начинается с начала диапазона и проходит до конца.
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
/// Записывает все совпадения, возникающие во время операции поиска и замены, в том порядке, в котором они происходили.
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

* enum [FindReplaceDirection](../../findreplacedirection/)
* class [FindReplaceOptions](../)
* пространство имен [Aspose.Words.Replacing](../../findreplaceoptions/)
* сборка [Aspose.Words](../../../)


