---
title: ReplacingArgs.GroupIndex
second_title: Справочник по API Aspose.Words для .NET
description: ReplacingArgs свойство. Идентифицирует по индексу захваченную группу вMatch  который необходимо заменить наReplacement строка.
type: docs
weight: 10
url: /ru/net/aspose.words.replacing/replacingargs/groupindex/
---
## ReplacingArgs.GroupIndex property

Идентифицирует по индексу захваченную группу в[`Match`](../match/) , который необходимо заменить на[`Replacement`](../replacement/) строка.

```csharp
public int GroupIndex { get; set; }
```

### Примечания

`GroupIndex` действует только тогда, когда[`GroupName`](../groupname/) нулевой.

По умолчанию ноль.

### Примеры

Показывает, как применить другой шрифт к новому содержимому с помощью FindReplaceOptions.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Font.Name = "Arial";
    builder.Writeln("Numbers that the find-and-replace operation will convert to hexadecimal and highlight:\n" +
                    "123, 456, 789 and 17379.");

    // Мы можем использовать объект «FindReplaceOptions», чтобы изменить процесс поиска и замены.
    FindReplaceOptions options = new FindReplaceOptions();

    // Установите для свойства HighlightColor цвет фона, который мы хотим применить к результирующему тексту операции.
    options.ApplyFont.HighlightColor = Color.LightGray;

    NumberHexer numberHexer = new NumberHexer();
    options.ReplacingCallback = numberHexer;

    int replacementCount = doc.Range.Replace(new Regex("[0-9]+"), "", options);

    Console.WriteLine(numberHexer.GetLog());

    Assert.AreEqual(4, replacementCount);
    Assert.AreEqual("Numbers that the find-and-replace operation will convert to hexadecimal and highlight:\r" +
                    "0x7B, 0x1C8, 0x315 and 0x43E3.", doc.GetText().Trim());
    Assert.AreEqual(4, doc.GetChildNodes(NodeType.Run, true).OfType<Run>()
            .Count(r => r.Font.HighlightColor.ToArgb() == Color.LightGray.ToArgb()));
}

/// <summary>
/// Заменяет числовые совпадения поиска и замены их шестнадцатеричными эквивалентами.
/// Ведет журнал каждой замены.
/// </summary>
private class NumberHexer : IReplacingCallback
{
    public ReplaceAction Replacing(ReplacingArgs args)
    {
        mCurrentReplacementNumber++;

        int number = Convert.ToInt32(args.Match.Value);

        args.Replacement = $"0x{number:X}";

        mLog.AppendLine($"Match #{mCurrentReplacementNumber}");
        mLog.AppendLine($"\tOriginal value:\t{args.Match.Value}");
        mLog.AppendLine($"\tReplacement:\t{args.Replacement}");
        mLog.AppendLine($"\tOffset in parent {args.MatchNode.NodeType} node:\t{args.MatchOffset}");

        mLog.AppendLine(string.IsNullOrEmpty(args.GroupName)
            ? $"\tGroup index:\t{args.GroupIndex}"
            : $"\tGroup name:\t{args.GroupName}");

        return ReplaceAction.Replace;
    }

    public string GetLog()
    {
        return mLog.ToString();
    }

    private int mCurrentReplacementNumber;
    private readonly StringBuilder mLog = new StringBuilder();
}
```

### Смотрите также

* class [ReplacingArgs](../)
* пространство имен [Aspose.Words.Replacing](../../replacingargs/)
* сборка [Aspose.Words](../../../)


