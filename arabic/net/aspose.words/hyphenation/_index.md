---
title: Hyphenation Class
linktitle: Hyphenation
articleTitle: Hyphenation
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Hyphenation لإدارة فعّالة لعلامات الوصل. حسّن مستنداتك بقواعد دقيقة خاصة بلغة معينة لعلامات الوصل.
type: docs
weight: 3580
url: /ar/net/aspose.words/hyphenation/
---
## Hyphenation class

يوفر طرقًا للتعامل مع قواميس الوصل. تحدد هذه القواميس أماكن استخدام كلمات لغة معينة.

لمعرفة المزيد، قم بزيارة[العمل مع الوصلات](https://docs.aspose.com/words/net/working-with-hyphenation/) مقالة توثيقية.

```csharp
public static class Hyphenation
```

## الخصائص

| اسم | وصف |
| --- | --- |
| static [Callback](../../aspose.words/hyphenation/callback/) { get; set; } | يحصل على واجهة الاتصال العكسي المستخدمة لطلب القواميس عند بناء تخطيط الصفحة للمستند أو يعينها. يسمح هذا بتأخير تحميل القواميس، وهو ما قد يكون مفيدًا عند معالجة المستندات بالعديد من اللغات. |
| static [WarningCallback](../../aspose.words/hyphenation/warningcallback/) { get; set; } | يتم استدعاؤها أثناء تحميل أنماط التهجئة، عندما يتم اكتشاف مشكلة قد تؤدي إلى فقدان دقة التنسيق. |

## طُرق

| اسم | وصف |
| --- | --- |
| static [IsDictionaryRegistered](../../aspose.words/hyphenation/isdictionaryregistered/)(*string*) | إرجاع`خطأ شنيع` إذا لم يكن هناك قاموس مسجل للغة المحددة أو إذا كان القاموس المسجل فارغًا،`حقيقي` وإلا. |
| static [RegisterDictionary](../../aspose.words/hyphenation/registerdictionary/#registerdictionary)(*string, Stream*) | يُسجِّل ويُحمِّل قاموس الواصلات للغة المُحدَّدة من دفق. يُرمى إذا تعذَّر قراءة القاموس أو كان تنسيقه غير صحيح. |
| static [RegisterDictionary](../../aspose.words/hyphenation/registerdictionary/#registerdictionary_1)(*string, string*) | يُسجِّل ويُحمِّل قاموس الواصلات للغة المُحدَّدة من الملف. يُرمى إذا تعذَّر قراءة القاموس أو كان تنسيقه غير صحيح. |
| static [UnregisterDictionary](../../aspose.words/hyphenation/unregisterdictionary/)(*string*) | يقوم بإلغاء تسجيل قاموس الوصل للغة المحددة. |

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

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
