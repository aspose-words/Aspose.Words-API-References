---
title: FindReplaceDirection Enum
linktitle: FindReplaceDirection
articleTitle: FindReplaceDirection
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Aspose.Words FindReplaceDirection لاستبدال النصوص بكفاءة. حسّن معالجة مستنداتك مع التحكم الدقيق في الاتجاه.
type: docs
weight: 5340
url: /ar/net/aspose.words.replacing/findreplacedirection/
---
## FindReplaceDirection enumeration

يحدد الاتجاه لعمليات الاستبدال.

```csharp
public enum FindReplaceDirection
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Forward | `0` | يتم استبدال العناصر المطابقة من الأول إلى الأخير. |
| Backward | `1` | يتم استبدال العناصر المطابقة من الأخير إلى الأول. |

## أمثلة

يوضح كيفية تحديد الاتجاه الذي تتحرك فيه عملية البحث والاستبدال في المستند.

```csharp
public void Direction(FindReplaceDirection findReplaceDirection)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // أدخل ثلاث عمليات تشغيل يمكننا البحث عنها باستخدام نمط التعبيرات العادية.
    // ضع أحد هذه العمليات داخل مربع النص.
    builder.Writeln("Match 1.");
    builder.Writeln("Match 2.");
    builder.Writeln("Match 3.");
    builder.Writeln("Match 4.");

    // يمكننا استخدام الكائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
    FindReplaceOptions options = new FindReplaceOptions();

    // تعيين استدعاء مخصص لخاصية "ReplacingCallback".
    TextReplacementRecorder callback = new TextReplacementRecorder();
    options.ReplacingCallback = callback;

    // اضبط خاصية "الاتجاه" على "FindReplaceDirection.Backward" للحصول على خاصية البحث والاستبدال
    // عملية البدء من نهاية النطاق، والعودة إلى البداية.
    // اضبط خاصية "الاتجاه" على "FindReplaceDirection.Forward" للحصول على خاصية البحث والاستبدال
    // عملية البدء من بداية النطاق والانتقال إلى النهاية.
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
/// يسجل جميع المطابقات التي تحدث أثناء عملية البحث والاستبدال بالترتيب الذي تحدث به.
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

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Replacing](../../aspose.words.replacing/)
* المجسم [Aspose.Words](../../)
