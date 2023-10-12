---
title: FindReplaceOptions.UseLegacyOrder
second_title: Aspose.Words لمراجع .NET API
description: FindReplaceOptions ملكية. يشير True إلى أن البحث عن النص يتم إجراؤه بشكل تسلسلي من الأعلى إلى الأسفل مع الأخذ في الاعتبار مربعات النص. القيمة الافتراضية هيخطأ شنيع .
type: docs
weight: 170
url: /ar/net/aspose.words.replacing/findreplaceoptions/uselegacyorder/
---
## FindReplaceOptions.UseLegacyOrder property

يشير True إلى أن البحث عن النص يتم إجراؤه بشكل تسلسلي من الأعلى إلى الأسفل مع الأخذ في الاعتبار مربعات النص. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool UseLegacyOrder { get; set; }
```

### أمثلة

يوضح كيفية تغيير ترتيب البحث للعقد عند إجراء عملية البحث عن النص واستبداله.

```csharp
public void UseLegacyOrder(bool useLegacyOrder)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // أدخل ثلاثة مسارات يمكننا البحث عنها باستخدام نمط التعبير العادي.
    // ضع أحد هذه العمليات داخل مربع نص.
    builder.Writeln("[tag 1]");
    Shape textBox = builder.InsertShape(ShapeType.TextBox, 100, 50);
    builder.Writeln("[tag 2]");
    builder.MoveTo(textBox.FirstParagraph);
    builder.Write("[tag 3]");

    // يمكننا استخدام كائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
    FindReplaceOptions options = new FindReplaceOptions();

    // قم بتعيين رد اتصال مخصص للخاصية "ReplacingCallback".
    TextReplacementTracker callback = new TextReplacementTracker();
    options.ReplacingCallback = callback;

    // إذا قمنا بتعيين الخاصية "UseLegacyOrder" على "صحيح"، فإن
    // ستتم عملية البحث والاستبدال عبر كافة عمليات التشغيل خارج مربع النص
    // قبل المرور على العناصر الموجودة داخل مربع النص.
    // إذا قمنا بتعيين خاصية "UseLegacyOrder" على "خطأ"، فإن
    // ستتم عملية البحث والاستبدال عبر جميع عمليات التشغيل في نطاق ما بترتيب تسلسلي.
    options.UseLegacyOrder = useLegacyOrder;

    doc.Range.Replace(new Regex(@"\[tag \d*\]"), "", options);

    Assert.AreEqual(useLegacyOrder ?
        new List<string> { "[tag 1]", "[tag 3]", "[tag 2]" } :
        new List<string> { "[tag 1]", "[tag 2]", "[tag 3]" }, callback.Matches);
}

/// <summary>
/// يسجل ترتيب جميع التطابقات التي تحدث أثناء عملية البحث والاستبدال.
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


