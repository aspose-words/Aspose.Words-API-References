---
title: ReplacingArgs.MatchOffset
second_title: Aspose.Words لمراجع .NET API
description: ReplacingArgs ملكية. يحصل على موضع البداية الصفري للمباراة من بداية العقدة التي تحتوي على بداية المباراة .
type: docs
weight: 50
url: /ar/net/aspose.words.replacing/replacingargs/matchoffset/
---
## ReplacingArgs.MatchOffset property

يحصل على موضع البداية الصفري للمباراة من بداية العقدة التي تحتوي على بداية المباراة .

```csharp
public int MatchOffset { get; }
```

### أمثلة

يوضح كيفية تطبيق خط مختلف على محتوى جديد عبر FindReplaceOptions.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Font.Name = "Arial";
    builder.Writeln("Numbers that the find-and-replace operation will convert to hexadecimal and highlight:\n" +
                    "123, 456, 789 and 17379.");

    // يمكننا استخدام كائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
    FindReplaceOptions options = new FindReplaceOptions();

    // اضبط خاصية "HighlightColor" على لون الخلفية الذي نريد تطبيقه على النص الناتج للعملية.
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
/// يستبدل مطابقات البحث والاستبدال الرقمية بمكافئاتها السداسية العشرية.
/// يحتفظ بسجل لكل بديل.
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

### أنظر أيضا

* class [ReplacingArgs](../)
* مساحة الاسم [Aspose.Words.Replacing](../../replacingargs/)
* المجسم [Aspose.Words](../../../)


