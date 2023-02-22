---
title: FindReplaceOptions.UseLegacyOrder
second_title: Aspose.Words لمراجع .NET API
description: FindReplaceOptions ملكية. تشير True إلى أن البحث عن نص يتم إجراؤه بالتتابع من أعلى إلى أسفل مع الأخذ في الاعتبار مربعات النص. القيمة الافتراضية هي false .
type: docs
weight: 150
url: /ar/net/aspose.words.replacing/findreplaceoptions/uselegacyorder/
---
## FindReplaceOptions.UseLegacyOrder property

تشير True إلى أن البحث عن نص يتم إجراؤه بالتتابع من أعلى إلى أسفل مع الأخذ في الاعتبار مربعات النص. القيمة الافتراضية هي false .

```csharp
public bool UseLegacyOrder { get; set; }
```

### أمثلة

يوضح كيفية تغيير ترتيب البحث في العقد عند تنفيذ عملية البحث والاستبدال النصية.

```csharp
[TestCase(true)] // ExSkip
[TestCase(false)] // ExSkip
public void UseLegacyOrder(bool useLegacyOrder)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // أدخل ثلاثة عمليات تشغيل يمكننا البحث عنها باستخدام نمط regex.
    // ضع واحدة من تلك التي تعمل داخل مربع نص.
    builder.Writeln("[tag 1]");
    Shape textBox = builder.InsertShape(ShapeType.TextBox, 100, 50);
    builder.Writeln("[tag 2]");
    builder.MoveTo(textBox.FirstParagraph);
    builder.Write("[tag 3]");

    // يمكننا استخدام كائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
    FindReplaceOptions options = new FindReplaceOptions();

    // تعيين رد اتصال مخصص لخاصية "ReplacingCallback".
    TextReplacementTracker callback = new TextReplacementTracker();
    options.ReplacingCallback = callback;

    // إذا قمنا بتعيين الخاصية "UseLegacyOrder" على "true" ، فإن ملف
    // ستمر عملية البحث والاستبدال في جميع عمليات التشغيل خارج مربع النص
    // قبل الانتقال إلى تلك الموجودة داخل مربع نص.
    // إذا قمنا بتعيين الخاصية "UseLegacyOrder" على "false" ، فإن ملف
    // البحث والاستبدال ستتجاوز جميع عمليات التشغيل في نطاق بترتيب تسلسلي.
    options.UseLegacyOrder = useLegacyOrder;

    doc.Range.Replace(new Regex(@"\[tag \d*\]"), "", options);

    Assert.AreEqual(useLegacyOrder ?
        new List<string> { "[tag 1]", "[tag 3]", "[tag 2]" } :
        new List<string> { "[tag 1]", "[tag 2]", "[tag 3]" }, callback.Matches);
}

/// <summary>
/// يسجل ترتيب كل التطابقات التي تحدث أثناء عملية البحث والاستبدال.
/// </summary>
private class TextReplacementTracker : IReplacingCallback
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

* class [FindReplaceOptions](../)
* مساحة الاسم [Aspose.Words.Replacing](../../findreplaceoptions/)
* المجسم [Aspose.Words](../../../)


