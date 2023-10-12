---
title: IHyphenationCallback.RequestDictionary
second_title: Aspose.Words لمراجع .NET API
description: IHyphenationCallback طريقة. لإعلام التطبيق بأنه لم يتم العثور على قاموس الواصلة للغة المحددة وقد يلزم تسجيله.
type: docs
weight: 10
url: /ar/net/aspose.words/ihyphenationcallback/requestdictionary/
---
## IHyphenationCallback.RequestDictionary method

لإعلام التطبيق بأنه لم يتم العثور على قاموس الواصلة للغة المحددة وقد يلزم تسجيله.

يجب أن يجد التنفيذ قاموسًا ويسجله باستخدامه[`RegisterDictionary`](../../hyphenation/registerdictionary/) طُرق.

إذا كان القاموس غير متاح لتطبيق اللغة المحددة، فيمكن إلغاء الاشتراك في المكالمات الإضافية لنفس اللغة باستخدام[`RegisterDictionary`](../../hyphenation/registerdictionary/) مع`باطل` القيمة.

```csharp
public void RequestDictionary(string language)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| language | String | اسم لغة، على سبيل المثال "en-US". راجع وثائق .NET لـ "اسم الثقافة" وRFC 4646 للحصول على التفاصيل. |

### ملاحظات

ستؤدي الاستثناءات التي يتم طرحها بهذه الطريقة إلى إحباط تنفيذ عملية تخطيط الصفحة.

### أمثلة

يوضح كيفية فتح وتسجيل قاموس من ملف.

```csharp
public void RegisterDictionary()
{
    // قم بإعداد رد اتصال يتتبع التحذيرات التي تحدث أثناء تسجيل قاموس الواصلة.
    WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
    Hyphenation.WarningCallback = warningInfoCollection;

    // قم بتسجيل قاموس الواصلة باللغة الإنجليزية (الولايات المتحدة) عن طريق الدفق.
    Stream dictionaryStream = new FileStream(MyDir + "hyph_en_US.dic", FileMode.Open);
    Hyphenation.RegisterDictionary("en-US", dictionaryStream);

    Assert.AreEqual(0, warningInfoCollection.Count);

    // افتح مستندًا باستخدام لغة لا يجوز لـ Microsoft Word تطبيق الواصلة عليها على جهاز إنجليزي، مثل الألمانية.
    Document doc = new Document(MyDir + "German text.docx");

    // لوصل هذا المستند عند الحفظ، نحتاج إلى قاموس وصل لرمز اللغة "de-CH".
    // سيتعامل رد الاتصال هذا مع الطلب التلقائي لهذا القاموس.
    Hyphenation.Callback = new CustomHyphenationDictionaryRegister();

    // عندما نحفظ المستند، ستصبح الواصلة الألمانية سارية المفعول.
    doc.Save(ArtifactsDir + "Hyphenation.RegisterDictionary.pdf");

    // يحتوي هذا القاموس على نمطين متطابقين، مما يؤدي إلى ظهور تحذير.
    Assert.AreEqual(1, warningInfoCollection.Count);
    Assert.AreEqual(WarningType.MinorFormattingLoss, warningInfoCollection[0].WarningType);
    Assert.AreEqual(WarningSource.Layout, warningInfoCollection[0].Source);
    Assert.AreEqual("Hyphenation dictionary contains duplicate patterns. The only first found pattern will be used. " +
                    "Content can be wrapped differently.", warningInfoCollection[0].Description);
}

/// <summary>
/// يربط رموز لغة ISO بأسماء ملفات النظام المحلي لملفات قاموس الواصلة.
/// </summary>
private class CustomHyphenationDictionaryRegister : IHyphenationCallback
{
    public CustomHyphenationDictionaryRegister()
    {
        mHyphenationDictionaryFiles = new Dictionary<string, string>
        {
            { "en-US", MyDir + "hyph_en_US.dic" },
            { "de-CH", MyDir + "hyph_de_CH.dic" }
        };
    }

    public void RequestDictionary(string language)
    {
        Console.Write("Hyphenation dictionary requested: " + language);

        if (Hyphenation.IsDictionaryRegistered(language))
        {
            Console.WriteLine(", is already registered.");
            return;
        }

        if (mHyphenationDictionaryFiles.ContainsKey(language))
        {
            Hyphenation.RegisterDictionary(language, mHyphenationDictionaryFiles[language]);
            Console.WriteLine(", successfully registered.");
            return;
        }

        Console.WriteLine(", no respective dictionary file known by this Callback.");
    }

    private readonly Dictionary<string, string> mHyphenationDictionaryFiles;
}
```

### أنظر أيضا

* interface [IHyphenationCallback](../)
* مساحة الاسم [Aspose.Words](../../ihyphenationcallback/)
* المجسم [Aspose.Words](../../../)


