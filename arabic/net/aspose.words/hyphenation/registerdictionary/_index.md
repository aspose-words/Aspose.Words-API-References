---
title: Hyphenation.RegisterDictionary
linktitle: RegisterDictionary
articleTitle: RegisterDictionary
second_title: Aspose.Words لـ .NET
description: حسّن معالجة النصوص بسهولة باستخدام طريقة Hyphenation RegisterDictionary. حمّل قواميس Hyphenation الخاصة بكل لغة بسلاسة لتحقيق أفضل النتائج.
type: docs
weight: 40
url: /ar/net/aspose.words/hyphenation/registerdictionary/
---
## RegisterDictionary(*string, Stream*) {#registerdictionary}

يُسجِّل ويُحمِّل قاموس الواصلات للغة المُحدَّدة من دفق. يُرمى إذا تعذَّر قراءة القاموس أو كان تنسيقه غير صحيح.

```csharp
public static void RegisterDictionary(string language, Stream stream)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| language | String | اسم لغة، مثل "en-US". راجع وثائق .NET لمعرفة "اسم الثقافة" وRFC 4646 لمزيد من التفاصيل. |
| stream | Stream | تدفق لملف القاموس بتنسيق OpenOffice. |

## أمثلة

يوضح كيفية فتح قاموس وتسجيله من ملف.

```csharp
public void RegisterDictionary()
{
    // قم بإعداد معاودة اتصال لتتبع التحذيرات التي تحدث أثناء تسجيل قاموس الوصل.
    WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
    Hyphenation.WarningCallback = warningInfoCollection;

    // قم بتسجيل قاموس الوصلات باللغة الإنجليزية (الولايات المتحدة) عن طريق التدفق.
    Stream dictionaryStream = new FileStream(MyDir + "hyph_en_US.dic", FileMode.Open);
    Hyphenation.RegisterDictionary("en-US", dictionaryStream);

    Assert.AreEqual(0, warningInfoCollection.Count);

    // افتح مستندًا بإعدادات محلية لا يمكن لـ Microsoft Word استخدامها مع أجهزة الكمبيوتر الإنجليزية، مثل الألمانية.
    Document doc = new Document(MyDir + "German text.docx");

    // لوضع علامة وصل على تلك الوثيقة عند الحفظ، نحتاج إلى قاموس علامات الوصل لكود اللغة "de-CH".
    // ستتولى وظيفة معاودة الاتصال هذه التعامل مع الطلب التلقائي لهذا القاموس.
    Hyphenation.Callback = new CustomHyphenationDictionaryRegister();

    // عندما نحفظ المستند، سيتم تطبيق الواصلة الألمانية.
    doc.Save(ArtifactsDir + "Hyphenation.RegisterDictionary.pdf");

    //يحتوي هذا القاموس على نمطين متطابقين، مما سيؤدي إلى إطلاق تحذير.
    Assert.AreEqual(1, warningInfoCollection.Count);
    Assert.AreEqual(WarningType.MinorFormattingLoss, warningInfoCollection[0].WarningType);
    Assert.AreEqual(WarningSource.Layout, warningInfoCollection[0].Source);
    Assert.AreEqual("Hyphenation dictionary contains duplicate patterns. The only first found pattern will be used. " +
                    "Content can be wrapped differently.", warningInfoCollection[0].Description);

}

/// <summary>
/// يربط أكواد لغة ISO بأسماء ملفات النظام المحلي لملفات قاموس الوصل.
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

يُسجِّل ويُحمِّل قاموس الواصلات للغة المُحدَّدة من الملف. يُرمى إذا تعذَّر قراءة القاموس أو كان تنسيقه غير صحيح.

يمكن أيضًا استخدام هذه الطريقة لتسجيل القاموس الفارغ لمنع[`Callback`](../callback/) من أن يتم استدعاؤها بشكل متكرر لنفس اللغة.

```csharp
public static void RegisterDictionary(string language, string fileName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| language | String | اسم لغة، مثل "en-US". راجع وثائق .NET لمعرفة "اسم الثقافة" وRFC 4646 لمزيد من التفاصيل. |
| fileName | String | المسار إلى ملف القاموس بتنسيق Open Office. |

## أمثلة

يوضح كيفية تسجيل قاموس الوصلات.

```csharp
//يحتوي قاموس الوصل على قائمة من السلاسل التي تحدد قواعد الوصل للغة القاموس.
// عندما تحتوي الوثيقة على أسطر نصية يمكن تقسيم الكلمة فيها ومتابعتها في السطر التالي،
// سوف يبحث الواصلة في قائمة القاموس الخاصة بالسلاسل عن السلاسل الفرعية لتلك الكلمة.
// إذا كان القاموس يحتوي على سلسلة فرعية، فإن الوصلة ستقسم الكلمة عبر سطرين
// بواسطة السلسلة الفرعية وأضف شرطة إلى النصف الأول.
// قم بتسجيل ملف القاموس من نظام الملفات المحلي إلى الإعدادات المحلية "de-CH".
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// افتح مستندًا يحتوي على نص بإعدادات محلية مطابقة لإعدادات القاموس لدينا،
// واحفظه بتنسيق صفحة ثابتة. سيتم وضع واصلة بين النص في هذا المستند.
Document doc = new Document(MyDir + "German text.docx");

Assert.True(doc.FirstSection.Body.FirstParagraph.Runs.OfType<Run>().All(
    r => r.Font.LocaleId == new CultureInfo("de-CH").LCID));

doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Registered.pdf");

// أعد تحميل المستند بعد إلغاء تسجيل القاموس،
// واحفظه في ملف PDF آخر، والذي لن يحتوي على نص به واصلة.
Hyphenation.UnregisterDictionary("de-CH");

Assert.False(Hyphenation.IsDictionaryRegistered("de-CH"));

doc = new Document(MyDir + "German text.docx");
doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Unregistered.pdf");
```

يوضح كيفية فتح قاموس وتسجيله من ملف.

```csharp
public void RegisterDictionary()
{
    // قم بإعداد معاودة اتصال لتتبع التحذيرات التي تحدث أثناء تسجيل قاموس الوصل.
    WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
    Hyphenation.WarningCallback = warningInfoCollection;

    // قم بتسجيل قاموس الوصلات باللغة الإنجليزية (الولايات المتحدة) عن طريق التدفق.
    Stream dictionaryStream = new FileStream(MyDir + "hyph_en_US.dic", FileMode.Open);
    Hyphenation.RegisterDictionary("en-US", dictionaryStream);

    Assert.AreEqual(0, warningInfoCollection.Count);

    // افتح مستندًا بإعدادات محلية لا يمكن لـ Microsoft Word استخدامها مع أجهزة الكمبيوتر الإنجليزية، مثل الألمانية.
    Document doc = new Document(MyDir + "German text.docx");

    // لوضع علامة وصل على تلك الوثيقة عند الحفظ، نحتاج إلى قاموس علامات الوصل لكود اللغة "de-CH".
    // ستتولى وظيفة معاودة الاتصال هذه التعامل مع الطلب التلقائي لهذا القاموس.
    Hyphenation.Callback = new CustomHyphenationDictionaryRegister();

    // عندما نحفظ المستند، سيتم تطبيق الواصلة الألمانية.
    doc.Save(ArtifactsDir + "Hyphenation.RegisterDictionary.pdf");

    //يحتوي هذا القاموس على نمطين متطابقين، مما سيؤدي إلى إطلاق تحذير.
    Assert.AreEqual(1, warningInfoCollection.Count);
    Assert.AreEqual(WarningType.MinorFormattingLoss, warningInfoCollection[0].WarningType);
    Assert.AreEqual(WarningSource.Layout, warningInfoCollection[0].Source);
    Assert.AreEqual("Hyphenation dictionary contains duplicate patterns. The only first found pattern will be used. " +
                    "Content can be wrapped differently.", warningInfoCollection[0].Description);

}

/// <summary>
/// يربط أكواد لغة ISO بأسماء ملفات النظام المحلي لملفات قاموس الوصل.
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
