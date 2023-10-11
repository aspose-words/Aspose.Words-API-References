---
title: FindReplaceOptions.Direction
second_title: Aspose.Words لمراجع .NET API
description: FindReplaceOptions ملكية. تحديد اتجاه الاستبدال. القيمة الافتراضية هيForward .
type: docs
weight: 40
url: /ar/net/aspose.words.replacing/findreplaceoptions/direction/
---
## FindReplaceOptions.Direction property

تحديد اتجاه الاستبدال. القيمة الافتراضية هيForward .

```csharp
public FindReplaceDirection Direction { get; set; }
```

### أمثلة

يوضح كيفية تحديد الاتجاه الذي تعبر فيه عملية البحث والاستبدال المستند.

```csharp
public void Direction(FindReplaceDirection findReplaceDirection)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // أدخل ثلاثة مسارات يمكننا البحث عنها باستخدام نمط التعبير العادي.
    // ضع أحد هذه العمليات داخل مربع نص.
    builder.Writeln("Match 1.");
    builder.Writeln("Match 2.");
    builder.Writeln("Match 3.");
    builder.Writeln("Match 4.");

    // يمكننا استخدام كائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
    FindReplaceOptions options = new FindReplaceOptions();

    // قم بتعيين رد اتصال مخصص للخاصية "ReplacingCallback".
    TextReplacementRecorder callback = new TextReplacementRecorder();
    options.ReplacingCallback = callback;

    // قم بتعيين خاصية "الاتجاه" على "FindReplaceDirection.Backward" للحصول على ميزة البحث والاستبدال
    // تبدأ العملية من نهاية النطاق وتعود إلى البداية.
    // قم بتعيين خاصية "الاتجاه" على "FindReplaceDirection.Backward" للحصول على ميزة البحث والاستبدال
    // تبدأ العملية من بداية النطاق وتجتازه حتى النهاية.
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
/// يسجل جميع التطابقات التي تحدث أثناء عملية البحث والاستبدال بالترتيب الذي تحدث به.
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

* enum [FindReplaceDirection](../../findreplacedirection/)
* class [FindReplaceOptions](../)
* مساحة الاسم [Aspose.Words.Replacing](../../findreplaceoptions/)
* المجسم [Aspose.Words](../../../)


