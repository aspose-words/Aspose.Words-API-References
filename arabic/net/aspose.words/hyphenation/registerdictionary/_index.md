---
title: RegisterDictionary
second_title: Aspose.Words لمراجع .NET API
description: يقوم بتسجيل وتحميل قاموس الواصلة للغة المحددة من الدفق. يتم رميه في حالة تعذر قراءة القاموس أو إذا كان تنسيقه غير صالح.
type: docs
weight: 40
url: /ar/net/aspose.words/hyphenation/registerdictionary/
---
## RegisterDictionary(string, Stream) {#registerdictionary}

يقوم بتسجيل وتحميل قاموس الواصلة للغة المحددة من الدفق. يتم رميه في حالة تعذر قراءة القاموس أو إذا كان تنسيقه غير صالح.

```csharp
public static void RegisterDictionary(string language, Stream stream)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| language | String | اسم اللغة ، على سبيل المثال "en-US". راجع وثائق .NET للحصول على "اسم الثقافة" و RFC 4646 للحصول على التفاصيل. |
| stream | Stream | دفق لملف القاموس بتنسيق OpenOffice. |

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

* class [Hyphenation](../../hyphenation)
* مساحة الاسم [Aspose.Words](../../hyphenation)
* المجسم [Aspose.Words](../../../)

---

## RegisterDictionary(string, string) {#registerdictionary_1}

يقوم بتسجيل وتحميل قاموس الواصلة للغة المحددة من الملف. يُطرح في حالة تعذر قراءة القاموس أو إذا كان تنسيقه غير صالح.

يمكن أيضًا استخدام هذه الطريقة لتسجيل قاموس Null لمنع حدوث ذلك[`Callback`](../callback) من الاستدعاء المتكرر لنفس اللغة ._ x000d_

```csharp
public static void RegisterDictionary(string language, string fileName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| language | String | اسم اللغة ، على سبيل المثال "en-US". راجع وثائق .NET للحصول على "اسم الثقافة" و RFC 4646 للحصول على التفاصيل. |
| fileName | String | مسار إلى ملف القاموس بتنسيق Open Office. |

### أمثلة

يوضح كيفية تسجيل قاموس الواصلة.

```csharp
// يحتوي قاموس الواصلة على قائمة بالسلاسل التي تحدد قواعد الواصلة للغة القاموس.
// عندما يحتوي المستند على سطور من النص يمكن فيها تقسيم الكلمة والاستمرار في السطر التالي ،
// ستبحث الواصلة في قائمة السلاسل في القاموس للسلاسل الفرعية لهذه الكلمة.
// إذا كان القاموس يحتوي على سلسلة فرعية ، فإن الواصلة ستقسم الكلمة على سطرين
// بواسطة السلسلة الفرعية وإضافة واصلة إلى النصف الأول.
// تسجيل ملف قاموس من نظام الملفات المحلي إلى لغة "de-CH".
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// افتح مستندًا يحتوي على نص بلغة تطابق لغة قاموسنا ،
// واحفظه في تنسيق حفظ بصفحة ثابتة. سيتم وصل النص الموجود في هذا المستند.
Document doc = new Document(MyDir + "German text.docx");

Assert.True(doc.FirstSection.Body.FirstParagraph.Runs.OfType<Run>().All(
    r => r.Font.LocaleId == new CultureInfo("de-CH").LCID));

doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Registered.pdf");

// أعد تحميل المستند بعد إلغاء تسجيل القاموس ،
// واحفظه في ملف PDF آخر ، والذي لن يحتوي على نصوص بواصلة.
Hyphenation.UnregisterDictionary("de-CH");

Assert.False(Hyphenation.IsDictionaryRegistered("de-CH"));

doc = new Document(MyDir + "German text.docx");
doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Unregistered.pdf");
```

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

* class [Hyphenation](../../hyphenation)
* مساحة الاسم [Aspose.Words](../../hyphenation)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
