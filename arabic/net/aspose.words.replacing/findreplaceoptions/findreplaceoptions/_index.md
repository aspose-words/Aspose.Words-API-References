---
title: FindReplaceOptions
linktitle: FindReplaceOptions
articleTitle: FindReplaceOptions
second_title: Aspose.Words لـ .NET
description: اكتشف منشئ FindReplaceOptions لتتمكن من تهيئة مثيل جديد بسهولة باستخدام الإعدادات الافتراضية، مما يعزز وظيفة البحث والاستبدال لديك.
type: docs
weight: 10
url: /ar/net/aspose.words.replacing/findreplaceoptions/findreplaceoptions/
---
## FindReplaceOptions() {#constructor}

يقوم بتهيئة مثيل جديد لفئة FindReplaceOptions باستخدام الإعدادات الافتراضية.

```csharp
public FindReplaceOptions()
```

## أمثلة

يوضح كيفية التعرف على الاستبدالات واستخدامها ضمن أنماط الاستبدال.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Jason gave money to Paul.");

Regex regex = new Regex(@"([A-z]+) gave money to ([A-z]+)");

FindReplaceOptions options = new FindReplaceOptions();
options.UseSubstitutions = true;

// إن استخدام الوضع القديم لا يدعم العديد من الميزات المتقدمة، لذا نحتاج إلى تعيينه على "خطأ".
options.LegacyMode = false;

doc.Range.Replace(regex, @"$2 took money from $1", options);

Assert.AreEqual(doc.GetText(), "Paul took money from Jason.\f");
```

### أنظر أيضا

* class [FindReplaceOptions](../)
* مساحة الاسم [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* المجسم [Aspose.Words](../../../)

---

## FindReplaceOptions(*[FindReplaceDirection](../../findreplacedirection/)*) {#constructor_1}

يقوم بتهيئة مثيل جديد لفئة FindReplaceOptions بالاتجاه المحدد.

```csharp
public FindReplaceOptions(FindReplaceDirection direction)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| direction | FindReplaceDirection | اتجاه عملية البحث والاستبدال. |

### أنظر أيضا

* enum [FindReplaceDirection](../../findreplacedirection/)
* class [FindReplaceOptions](../)
* مساحة الاسم [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* المجسم [Aspose.Words](../../../)

---

## FindReplaceOptions(*[IReplacingCallback](../../ireplacingcallback/)*) {#constructor_3}

يقوم بتهيئة مثيل جديد لفئة FindReplaceOptions باستخدام استدعاء الاستبدال المحدد.

```csharp
public FindReplaceOptions(IReplacingCallback replacingCallback)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| replacingCallback | IReplacingCallback | استدعاء يتم استخدامه لاستبدال النص الموجود. |

## أمثلة

يوضح كيفية تتبع الترتيب الذي تمر به عملية استبدال النص عبر العقد.

```csharp
public void Order(bool differentFirstPageHeaderFooter)
{
    Document doc = new Document(MyDir + "Header and footer types.docx");

    Section firstPageSection = doc.FirstSection;

    ReplaceLog logger = new ReplaceLog();
    FindReplaceOptions options = new FindReplaceOptions(logger);

    // استخدام رأس/تذييل مختلف للصفحة الأولى سيؤثر على ترتيب البحث.
    firstPageSection.PageSetup.DifferentFirstPageHeaderFooter = differentFirstPageHeaderFooter;
    doc.Range.Replace(new Regex("(header|footer)"), "", options);

    if (differentFirstPageHeaderFooter)
        Assert.AreEqual("First header\nFirst footer\nSecond header\nSecond footer\nThird header\nThird footer\n", 
            logger.Text.Replace("\r", ""));
    else
        Assert.AreEqual("Third header\nFirst header\nThird footer\nFirst footer\nSecond header\nSecond footer\n", 
            logger.Text.Replace("\r", ""));
}

/// <summary>
/// أثناء عملية البحث والاستبدال، يتم تسجيل محتويات كل عقدة تحتوي على نص "تجده" العملية،
/// في الحالة التي كانت عليها قبل أن يتم الاستبدال.
/// سيؤدي هذا إلى عرض الترتيب الذي تمر به عملية استبدال النص عبر العقد.
/// </summary>
private class ReplaceLog : IReplacingCallback
{
    public ReplaceAction Replacing(ReplacingArgs args)
    {
        mTextBuilder.AppendLine(args.MatchNode.GetText());
        return ReplaceAction.Skip;
    }

    internal string Text => mTextBuilder.ToString();

    private readonly StringBuilder mTextBuilder = new StringBuilder();
}
```

### أنظر أيضا

* interface [IReplacingCallback](../../ireplacingcallback/)
* class [FindReplaceOptions](../)
* مساحة الاسم [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* المجسم [Aspose.Words](../../../)

---

## FindReplaceOptions(*[FindReplaceDirection](../../findreplacedirection/), [IReplacingCallback](../../ireplacingcallback/)*) {#constructor_2}

يقوم بتهيئة مثيل جديد لفئة FindReplaceOptions بالاتجاه المحدد واستدعاء الاستبدال.

```csharp
public FindReplaceOptions(FindReplaceDirection direction, IReplacingCallback replacingCallback)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| direction | FindReplaceDirection | اتجاه عملية البحث والاستبدال. |
| replacingCallback | IReplacingCallback | استدعاء يتم استخدامه لاستبدال النص الموجود. |

### أنظر أيضا

* enum [FindReplaceDirection](../../findreplacedirection/)
* interface [IReplacingCallback](../../ireplacingcallback/)
* class [FindReplaceOptions](../)
* مساحة الاسم [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* المجسم [Aspose.Words](../../../)
