---
title: FindReplaceOptions.UseLegacyOrder
linktitle: UseLegacyOrder
articleTitle: UseLegacyOrder
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية UseLegacyOrder في FindReplaceOptions. فعّل عمليات البحث النصية المتسلسلة لتحسين الدقة. الإعداد الافتراضي هو خطأ. حسّن معالجة النصوص لديك!
type: docs
weight: 180
url: /ar/net/aspose.words.replacing/findreplaceoptions/uselegacyorder/
---
## FindReplaceOptions.UseLegacyOrder property

يشير True إلى أن البحث عن النص يتم بشكل تسلسلي من الأعلى إلى الأسفل مع مراعاة مربعات النص. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool UseLegacyOrder { get; set; }
```

## أمثلة

يوضح كيفية تغيير ترتيب البحث للعقد عند تنفيذ عملية البحث والاستبدال للنص.

```csharp
public void UseLegacyOrder(bool useLegacyOrder)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // أدخل ثلاث عمليات تشغيل يمكننا البحث عنها باستخدام نمط التعبيرات العادية.
    // ضع أحد هذه العمليات داخل مربع النص.
    builder.Writeln("[tag 1]");
    Shape textBox = builder.InsertShape(ShapeType.TextBox, 100, 50);
    builder.Writeln("[tag 2]");
    builder.MoveTo(textBox.FirstParagraph);
    builder.Write("[tag 3]");

    // يمكننا استخدام الكائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
    FindReplaceOptions options = new FindReplaceOptions();

    // تعيين استدعاء مخصص لخاصية "ReplacingCallback".
    TextReplacementTracker callback = new TextReplacementTracker();
    options.ReplacingCallback = callback;

    // إذا قمنا بتعيين خاصية "UseLegacyOrder" إلى "true"،
    // ستمر عملية البحث والاستبدال عبر جميع عمليات التشغيل خارج مربع النص
    // قبل المرور على العناصر الموجودة داخل مربع النص.
    // إذا قمنا بتعيين خاصية "UseLegacyOrder" إلى "false"،
    // ستعمل عملية البحث والاستبدال على تنفيذ جميع عمليات التشغيل في نطاق معين بالترتيب التسلسلي.
    options.UseLegacyOrder = useLegacyOrder;

    doc.Range.Replace(new Regex(@"\[tag \d*\]"), "", options);

    Assert.AreEqual(useLegacyOrder ?
        new List<string> { "[tag 1]", "[tag 3]", "[tag 2]" } :
        new List<string> { "[tag 1]", "[tag 2]", "[tag 3]" }, callback.Matches);
}

/// <summary>
/// يسجل ترتيب جميع المطابقات التي تحدث أثناء عملية البحث والاستبدال.
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
* مساحة الاسم [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* المجسم [Aspose.Words](../../../)
