---
title: ReplacingArgs.Replacement
second_title: Aspose.Words لمراجع .NET API
description: ReplacingArgs ملكية. الحصول على سلسلة الاستبدال أو تعيينها.
type: docs
weight: 60
url: /ar/net/aspose.words.replacing/replacingargs/replacement/
---
## ReplacingArgs.Replacement property

الحصول على سلسلة الاستبدال أو تعيينها.

```csharp
public string Replacement { get; set; }
```

### أمثلة

يوضح كيفية استبدال كل تكرارات نمط التعبير العادي بسلسلة أخرى ، أثناء تتبع كل هذه الاستبدالات.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("Our new location in New York City is opening tomorrow. " +
                    "Hope to see all our NYC-based customers at the opening!");

    // يمكننا استخدام كائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
    FindReplaceOptions options = new FindReplaceOptions();

    // تعيين رد اتصال يتتبع أي بدائل تقوم بها طريقة "استبدال".
    TextFindAndReplacementLogger logger = new TextFindAndReplacementLogger();
    options.ReplacingCallback = logger;

    doc.Range.Replace(new Regex("New York City|NYC"), "Washington", options);

    Assert.AreEqual("Our new location in (Old value:\"New York City\") Washington is opening tomorrow. " +
                    "Hope to see all our (Old value:\"NYC\") Washington-based customers at the opening!", doc.GetText().Trim());

    Assert.AreEqual("\"New York City\" converted to \"Washington\" 20 characters into a Run node.\r\n" +
                    "\"NYC\" converted to \"Washington\" 42 characters into a Run node.", logger.GetLog().Trim());
}

/// <summary>
/// يحتفظ بسجل لكل استبدال نص يتم إجراؤه بواسطة عملية البحث والاستبدال
/// ويلاحظ قيمة النص المتطابق الأصلي.
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

### أنظر أيضا

* class [ReplacingArgs](../)
* مساحة الاسم [Aspose.Words.Replacing](../../replacingargs/)
* المجسم [Aspose.Words](../../../)


