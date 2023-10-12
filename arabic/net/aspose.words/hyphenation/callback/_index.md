---
title: Hyphenation.Callback
second_title: Aspose.Words لمراجع .NET API
description: Hyphenation ملكية. الحصول على أو تعيين واجهة رد الاتصال المستخدمة لطلب القواميس عند إنشاء تخطيط صفحة المستند. وهذا يسمح بتأخير تحميل القواميس مما قد يكون مفيدًا عند معالجة المستندات بالعديد من اللغات.
type: docs
weight: 10
url: /ar/net/aspose.words/hyphenation/callback/
---
## Hyphenation.Callback property

الحصول على أو تعيين واجهة رد الاتصال المستخدمة لطلب القواميس عند إنشاء تخطيط صفحة المستند. وهذا يسمح بتأخير تحميل القواميس مما قد يكون مفيدًا عند معالجة المستندات بالعديد من اللغات.

```csharp
public static IHyphenationCallback Callback { get; set; }
```

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

* interface [IHyphenationCallback](../../ihyphenationcallback/)
* class [Hyphenation](../)
* مساحة الاسم [Aspose.Words](../../hyphenation/)
* المجسم [Aspose.Words](../../../)


