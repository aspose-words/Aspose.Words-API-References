---
title: Class Hyphenation
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Hyphenation فصل. يوفر طرقًا للعمل مع قواميس الواصلة. تصف هذه القواميس المكان الذي يمكن فيه وصل كلمات لغة معينة.
type: docs
weight: 3150
url: /ar/net/aspose.words/hyphenation/
---
## Hyphenation class

يوفر طرقًا للعمل مع قواميس الواصلة. تصف هذه القواميس المكان الذي يمكن فيه وصل كلمات لغة معينة.

لمعرفة المزيد، قم بزيارة[العمل مع الواصلة](https://docs.aspose.com/words/net/working-with-hyphenation/) مقالة توثيقية.

```csharp
public static class Hyphenation
```

## الخصائص

| اسم | وصف |
| --- | --- |
| static [Callback](../../aspose.words/hyphenation/callback/) { get; set; } | الحصول على أو تعيين واجهة رد الاتصال المستخدمة لطلب القواميس عند إنشاء تخطيط صفحة المستند. وهذا يسمح بتأخير تحميل القواميس مما قد يكون مفيدًا عند معالجة المستندات بالعديد من اللغات. |
| static [WarningCallback](../../aspose.words/hyphenation/warningcallback/) { get; set; } | يتم استدعاؤه أثناء تحميل أنماط الواصلة، عند اكتشاف مشكلة قد تؤدي إلى فقدان دقة التنسيق. |

## طُرق

| اسم | وصف |
| --- | --- |
| static [IsDictionaryRegistered](../../aspose.words/hyphenation/isdictionaryregistered/)(string) | إرجاع`خطأ شنيع` إذا لم يكن هناك قاموس مسجل للغة المحددة أو إذا كان المسجل هو قاموس فارغ،`حقيقي` وإلا. |
| static [RegisterDictionary](../../aspose.words/hyphenation/registerdictionary/#registerdictionary)(string, Stream) | يقوم بتسجيل وتحميل قاموس الواصلة للغة المحددة من الدفق. يتم الرمي إذا تعذرت قراءة القاموس أو كان تنسيقه غير صالح. |
| static [RegisterDictionary](../../aspose.words/hyphenation/registerdictionary/#registerdictionary_1)(string, string) | يقوم بتسجيل وتحميل قاموس الواصلة للغة المحددة من الملف. يتم الرمي إذا تعذرت قراءة القاموس أو كان تنسيقه غير صالح. |
| static [UnregisterDictionary](../../aspose.words/hyphenation/unregisterdictionary/)(string) | إلغاء تسجيل قاموس الواصلة للغة المحددة. |

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

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)


