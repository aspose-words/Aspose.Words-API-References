---
title: ReplacingArgs.GroupIndex
linktitle: GroupIndex
articleTitle: GroupIndex
second_title: Aspose.Words لـ .NET
description: تعرف على كيفية استخدام خاصية GroupIndex في ReplacingArgs لتحديد المجموعات الملتقطة واستبدالها بسهولة في المطابقات باستخدام السلاسل المخصصة لديك.
type: docs
weight: 10
url: /ar/net/aspose.words.replacing/replacingargs/groupindex/
---
## ReplacingArgs.GroupIndex property

يحدد، عن طريق الفهرس، المجموعة الملتقطة في[`Match`](../match/) الذي سيتم استبداله بـ[`Replacement`](../replacement/) سلسلة.

```csharp
public int GroupIndex { get; set; }
```

## ملاحظات

`GroupIndex` لا يكون له تأثير إلا عندما[`GroupName`](../groupname/) يكون`باطل`.

الإفتراضي هو صفر.

## أمثلة

يوضح كيفية تطبيق خط مختلف على محتوى جديد عبر FindReplaceOptions.

```csharp
public void ConvertNumbersToHexadecimal()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Font.Name = "Arial";
    builder.Writeln("Numbers that the find-and-replace operation will convert to hexadecimal and highlight:\n" +
                    "123, 456, 789 and 17379.");

    // يمكننا استخدام الكائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
    FindReplaceOptions options = new FindReplaceOptions();

    // قم بتعيين خاصية "HighlightColor" إلى لون الخلفية الذي نريد تطبيقه على النص الناتج عن العملية.
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
/// استبدال تطابقات البحث والاستبدال الرقمية بمكافئاتها السداسية عشرية.
/// يحتفظ بسجل لكل عملية استبدال.
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
* مساحة الاسم [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* المجسم [Aspose.Words](../../../)
