---
title: Hyphenation.RegisterDictionary
linktitle: RegisterDictionary
articleTitle: RegisterDictionary
second_title: Aspose.Words لـ .NET
description: Hyphenation RegisterDictionary طريقة. يقوم بتسجيل وتحميل قاموس الواصلة للغة المحددة من الدفق. يتم الرمي إذا تعذرت قراءة القاموس أو كان تنسيقه غير صالح في C#.
type: docs
weight: 40
url: /ar/net/aspose.words/hyphenation/registerdictionary/
---
## RegisterDictionary(*string, Stream*) {#registerdictionary}

يقوم بتسجيل وتحميل قاموس الواصلة للغة المحددة من الدفق. يتم الرمي إذا تعذرت قراءة القاموس أو كان تنسيقه غير صالح.

```csharp
public static void RegisterDictionary(string language, Stream stream)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| language | String | اسم لغة، على سبيل المثال "en-US". راجع وثائق .NET لـ "اسم الثقافة" وRFC 4646 للحصول على التفاصيل. |
| stream | Stream | دفق لملف القاموس بتنسيق OpenOffice. |

## أمثلة

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

* class [Hyphenation](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## RegisterDictionary(*string, string*) {#registerdictionary_1}

يقوم بتسجيل وتحميل قاموس الواصلة للغة المحددة من الملف. يتم الرمي إذا تعذرت قراءة القاموس أو كان تنسيقه غير صالح.

يمكن أيضًا استخدام هذه الطريقة لتسجيل القاموس الفارغ لمنعه[`Callback`](../callback/) من أن يتم استدعاؤك بشكل متكرر بنفس اللغة.

```csharp
public static void RegisterDictionary(string language, string fileName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| language | String | اسم لغة، على سبيل المثال "en-US". راجع وثائق .NET لـ "اسم الثقافة" وRFC 4646 للحصول على التفاصيل. |
| fileName | String | مسار إلى ملف القاموس بتنسيق Open Office. |

## أمثلة

يوضح كيفية تسجيل قاموس الواصلة.

```csharp
// يحتوي قاموس الواصلة على قائمة من السلاسل التي تحدد قواعد الواصلة للغة القاموس.
// عندما يحتوي المستند على أسطر نصية يمكن فيها تقسيم الكلمة واستمرارها في السطر التالي،
// ستبحث الواصلة في قائمة سلاسل القاموس عن السلاسل الفرعية لتلك الكلمة.
// إذا كان القاموس يحتوي على سلسلة فرعية، فستؤدي الواصلة إلى تقسيم الكلمة عبر سطرين
// بواسطة السلسلة الفرعية وأضف واصلة إلى النصف الأول.
// سجل ملف قاموس من نظام الملفات المحلي إلى لغة "de-CH".
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// افتح مستندًا يحتوي على نص ذو لغة تطابق لغة القاموس الخاص بنا،
// وحفظه بتنسيق حفظ صفحة ثابتة. سيتم تطبيق الواصلة على النص الموجود في هذا المستند.
Document doc = new Document(MyDir + "German text.docx");

Assert.True(doc.FirstSection.Body.FirstParagraph.Runs.OfType<Run>().All(
    r => r.Font.LocaleId == new CultureInfo("de-CH").LCID));

doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Registered.pdf");

// أعد تحميل المستند بعد إلغاء تسجيل القاموس،
// واحفظه في ملف PDF آخر، والذي لن يحتوي على نص موصول.
Hyphenation.UnregisterDictionary("de-CH");

Assert.False(Hyphenation.IsDictionaryRegistered("de-CH"));

doc = new Document(MyDir + "German text.docx");
doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Unregistered.pdf");
```

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

* class [Hyphenation](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
