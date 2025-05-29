---
title: IHyphenationCallback.RequestDictionary
linktitle: RequestDictionary
articleTitle: RequestDictionary
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة IHyphenationCallback RequestDictionary، وقم بالتعامل بكفاءة مع قواميس الوصل المفقودة للحصول على دعم لغوي سلس في تطبيقك.
type: docs
weight: 10
url: /ar/net/aspose.words/ihyphenationcallback/requestdictionary/
---
## IHyphenationCallback.RequestDictionary method

يُعلم التطبيق بأنه لم يتم العثور على قاموس الوصل للغة المحددة وقد يحتاج إلى التسجيل.

يجب على التنفيذ العثور على قاموس وتسجيله باستخدام[`RegisterDictionary`](../../hyphenation/registerdictionary/) طُرق.

إذا لم يكن القاموس متاحًا للغة المحددة، فيمكن إلغاء الاشتراك في المزيد من المكالمات لنفس اللغة باستخدام[`RegisterDictionary`](../../hyphenation/registerdictionary/) مع`باطل` القيمة.

```csharp
public void RequestDictionary(string language)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| language | String | اسم لغة، مثل "en-US". راجع وثائق .NET لمعرفة "اسم الثقافة" وRFC 4646 لمزيد من التفاصيل. |

## ملاحظات

ستؤدي الاستثناءات التي تم طرحها بواسطة هذه الطريقة إلى إلغاء تنفيذ عملية تخطيط الصفحة.

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

* interface [IHyphenationCallback](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
