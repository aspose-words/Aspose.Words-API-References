---
title: Enum MsWordVersion
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Settings.MsWordVersion تعداد. يسمح لـ Aspose.Wods بتقليد سلوك التطبيق الخاص بإصدار MS Word.
type: docs
weight: 5560
url: /ar/net/aspose.words.settings/mswordversion/
---
## MsWordVersion enumeration

يسمح لـ Aspose.Wods بتقليد سلوك التطبيق الخاص بإصدار MS Word.

```csharp
public enum MsWordVersion
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Word2000 | `0` | تحسين سلوك Aspose.Words لمطابقة إصدار MS Word 2000. |
| Word2002 | `1` | تحسين سلوك Aspose.Words لمطابقة إصدار MS Word 2002. |
| Word2003 | `2` | تحسين سلوك Aspose.Words لمطابقة إصدار MS Word 2003. |
| Word2007 | `3` | تحسين سلوك Aspose.Words لمطابقة إصدار MS Word 2007. |
| Word2010 | `4` | تحسين سلوك Aspose.Words لمطابقة إصدار MS Word 2010. |
| Word2013 | `5` | تحسين سلوك Aspose.Words لمطابقة إصدار MS Word 2013. |
| Word2016 | `6` | تحسين سلوك Aspose.Words لمطابقة إصدار MS Word 2016. |
| Word2019 | `7` | تحسين سلوك Aspose.Words لمطابقة إصدار MS Word 2019. |

### أمثلة

يوضح كيفية تحسين المستند لإصدارات مختلفة من Microsoft Word.

```csharp
public void OptimizeFor()
{
    Document doc = new Document();

    // يحتوي هذا الكائن على قائمة واسعة من العلامات الفريدة لكل مستند
    // التي تسمح لنا بتسهيل التوافق مع الإصدارات القديمة من Microsoft Word.
    CompatibilityOptions options = doc.CompatibilityOptions;

    // طباعة الإعدادات الافتراضية لمستند فارغ.
    Console.WriteLine("\nDefault optimization settings:");
    PrintCompatibilityOptions(options);

    // يمكننا الوصول إلى هذه الإعدادات في Microsoft Word عبر "ملف" - >; "خيارات" - >. "متقدم" - >. "خيارات التوافق لـ ...".
    doc.Save(ArtifactsDir + "CompatibilityOptions.OptimizeFor.DefaultSettings.docx");

    // يمكننا استخدام طريقة OptimizeFor لضمان التوافق الأمثل مع إصدار معين من Microsoft Word.
    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2010);
    Console.WriteLine("\nOptimized for Word 2010:");
    PrintCompatibilityOptions(options);

    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2000);
    Console.WriteLine("\nOptimized for Word 2000:");
    PrintCompatibilityOptions(options);
}

/// <summary>
/// يجمع كل العلامات في كائن خيارات توافق المستند حسب الحالة ، ثم يطبع كل مجموعة.
/// </summary>
private static void PrintCompatibilityOptions(CompatibilityOptions options)
{
    for (int i = 1; i >= 0; i--)
    {
        Console.WriteLine(Convert.ToBoolean(i) ? "\tEnabled options:" : "\tDisabled options:");
        SortedSet<string> optionNames = new SortedSet<string>();

        foreach (System.ComponentModel.PropertyDescriptor descriptor in System.ComponentModel.TypeDescriptor.GetProperties(options))
        {
            if (descriptor.PropertyType == Type.GetType("System.Boolean") && i == Convert.ToInt32(descriptor.GetValue(options)))
            {
                optionNames.Add(descriptor.Name);
            }
        }

        foreach (string s in optionNames)
        {
            Console.WriteLine($"\t\t{s}");
        }
    }
}
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Settings](../../aspose.words.settings/)
* المجسم [Aspose.Words](../../)


