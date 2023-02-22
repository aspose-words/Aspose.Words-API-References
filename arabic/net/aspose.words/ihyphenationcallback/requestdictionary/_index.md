---
title: IHyphenationCallback.RequestDictionary
second_title: Aspose.Words لمراجع .NET API
description: IHyphenationCallback طريقة. يخطر التطبيق بأنه لم يتم العثور على قاموس الواصلة للغة المحددة وقد يحتاج إلى التسجيل.
type: docs
weight: 10
url: /ar/net/aspose.words/ihyphenationcallback/requestdictionary/
---
## IHyphenationCallback.RequestDictionary method

يخطر التطبيق بأنه لم يتم العثور على قاموس الواصلة للغة المحددة وقد يحتاج إلى التسجيل.

يجب أن يجد التنفيذ قاموسًا ويسجله باستخدامه[`RegisterDictionary`](../../hyphenation/registerdictionary/)طُرق.

إذا كان القاموس غير متاح لتطبيق اللغة المحدد ، فيمكن إلغاء الاشتراك في المكالمات الإضافية لنفس اللغة_ باستخدام[`RegisterDictionary`](../../hyphenation/registerdictionary/) بقيمة فارغة.

```csharp
public void RequestDictionary(string language)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| language | String | اسم اللغة ، على سبيل المثال "en-US". راجع وثائق .NET للحصول على "اسم الثقافة" و RFC 4646 للحصول على التفاصيل. |

### ملاحظات

ستؤدي الاستثناءات التي يتم طرحها بواسطة هذه الطريقة إلى إحباط تنفيذ عملية تخطيط الصفحة.

### أمثلة

يوضح كيفية فتح وتسجيل قاموس من ملف.

```csharp
{
    // إعداد رد اتصال يتتبع التحذيرات التي تحدث أثناء تسجيل قاموس الواصلة.
    WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
    Hyphenation.WarningCallback = warningInfoCollection;

    // تسجيل قاموس الواصلة باللغة الإنجليزية (الولايات المتحدة) عن طريق الدفق.
    Stream dictionaryStream = new FileStream(MyDir + "hyph_en_US.dic", FileMode.Open);
    Hyphenation.RegisterDictionary("en-US", dictionaryStream);

    Assert.AreEqual(0, warningInfoCollection.Count);

    // افتح مستندًا بإعدادات محلية قد لا يقوم Microsoft Word بربطها على جهاز باللغة الإنجليزية ، مثل الألمانية.
    Document doc = new Document(MyDir + "German text.docx");

    // لوصل هذا المستند عند الحفظ ، نحتاج إلى قاموس الواصلة لرمز اللغة "de-CH".
    // سيعالج رد النداء هذا الطلب التلقائي لهذا القاموس.
    Hyphenation.Callback = new CustomHyphenationDictionaryRegister();

    // عندما نحفظ المستند ، سيتم تفعيل الواصلة الألمانية.
    doc.Save(ArtifactsDir + "Hyphenation.RegisterDictionary.pdf");

    // يحتوي هذا القاموس على نمطين متطابقين ، مما يؤدي إلى إطلاق تحذير.
    Assert.AreEqual(1, warningInfoCollection.Count);
    Assert.AreEqual(WarningType.MinorFormattingLoss, warningInfoCollection[0].WarningType);
    Assert.AreEqual(WarningSource.Layout, warningInfoCollection[0].Source);
    Assert.AreEqual("Hyphenation dictionary contains duplicate patterns. The only first found pattern will be used. " +
                    "Content can be wrapped differently.", warningInfoCollection[0].Description);
}

/// <summary>
/// تربط رموز لغة ISO بأسماء ملفات النظام المحلي لملفات قاموس الواصلة.
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


