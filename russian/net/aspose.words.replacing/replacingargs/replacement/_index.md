---
title: ReplacingArgs.Replacement
second_title: Справочник по API Aspose.Words для .NET
description: ReplacingArgs свойство. Получает или задает строку замены.
type: docs
weight: 60
url: /ru/net/aspose.words.replacing/replacingargs/replacement/
---
## ReplacingArgs.Replacement property

Получает или задает строку замены.

```csharp
public string Replacement { get; set; }
```

### Примеры

Показывает, как заменить все вхождения шаблона регулярного выражения другой строкой, отслеживая при этом все такие замены.

```csharp
public void ReplaceWithCallback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("Our new location in New York City is opening tomorrow. " +
                    "Hope to see all our NYC-based customers at the opening!");

    // Мы можем использовать объект «FindReplaceOptions» для изменения процесса поиска и замены.
    FindReplaceOptions options = new FindReplaceOptions();

    // Установите обратный вызов, который отслеживает любые замены, которые сделает метод "Replace".
    TextFindAndReplacementLogger logger = new TextFindAndReplacementLogger();
    options.ReplacingCallback = logger;

    doc.Range.Replace(new Regex("New York City|NYC"), "Washington", options);

    Assert.AreEqual("Our new location in (Old value:\"New York City\") Washington is opening tomorrow. " +
                    "Hope to see all our (Old value:\"NYC\") Washington-based customers at the opening!", doc.GetText().Trim());

    Assert.AreEqual("\"New York City\" converted to \"Washington\" 20 characters into a Run node.\r\n" +
                    "\"NYC\" converted to \"Washington\" 42 characters into a Run node.", logger.GetLog().Trim());
}

/// <summary>
/// Ведёт журнал каждой замены текста, выполненной операцией поиска и замены
/// и отмечает значение исходного совпавшего текста.
/// </summary>
private class TextFindAndReplacementLogger : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs args)
    {
        mLog.AppendLine($"\"{args.Match.Value}\" converted to \"{args.Replacement}\" " +
                        $"{args.MatchOffset} characters into a {args.MatchNode.NodeType} node.");

        args.Replacement = $"(Old value:\"{args.Match.Value}\") {args.Replacement}";
        return ReplaceAction.Replace;
    }

    public string GetLog()
    {
        return mLog.ToString();
    }

    private readonly StringBuilder mLog = new StringBuilder();
}
```

### Смотрите также

* class [ReplacingArgs](../)
* пространство имен [Aspose.Words.Replacing](../../replacingargs/)
* сборка [Aspose.Words](../../../)


