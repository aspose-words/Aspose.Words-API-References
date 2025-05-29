---
title: ReplacingArgs.Replacement
linktitle: Replacement
articleTitle: Replacement
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية الاستبدال ReplacingArgs لإدارة سلاسل الاستبدال وتخصيصها بسهولة لتحسين كفاءة الترميز.
type: docs
weight: 60
url: /ar/net/aspose.words.replacing/replacingargs/replacement/
---
## ReplacingArgs.Replacement property

يحصل على سلسلة الاستبدال أو يعينها.

```csharp
public string Replacement { get; set; }
```

## أمثلة

يوضح كيفية استبدال جميع حالات نمط التعبير العادي بسلسلة أخرى، مع تتبع كل هذه الاستبدالات.

```csharp
public void ReplaceWithCallback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("Our new location in New York City is opening tomorrow. " +
                    "Hope to see all our NYC-based customers at the opening!");

    // يمكننا استخدام الكائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
    FindReplaceOptions options = new FindReplaceOptions();

    // قم بتعيين معاودة الاتصال لتتبع أي عمليات استبدال ستقوم بها طريقة "الاستبدال".
    TextFindAndReplacementLogger logger = new TextFindAndReplacementLogger();
    options.ReplacingCallback = logger;

    doc.Range.Replace(new Regex("New York City|NYC"), "Washington", options);

    Assert.AreEqual("Our new location in (Old value:\"New York City\") Washington is opening tomorrow. " +
                    "Hope to see all our (Old value:\"NYC\") Washington-based customers at the opening!", doc.GetText().Trim());

    Assert.AreEqual("\"New York City\" converted to \"Washington\" 20 characters into a Run node.\r\n" +
                    "\"NYC\" converted to \"Washington\" 42 characters into a Run node.", logger.GetLog().Trim());
}

/// <summary>
/// يحتفظ بسجل لكل استبدال نص تم إجراؤه بواسطة عملية البحث والاستبدال
/// ويلاحظ قيمة النص المطابق الأصلي.
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
* مساحة الاسم [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* المجسم [Aspose.Words](../../../)
