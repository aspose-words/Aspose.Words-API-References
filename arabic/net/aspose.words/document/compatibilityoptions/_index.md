---
title: Document.CompatibilityOptions
second_title: Aspose.Words لمراجع .NET API
description: Document ملكية. يوفر الوصول إلى خيارات توافق المستندات أي تفضيلات المستخدم التي تم إدخالها في ملف التوافق علامة التبويب خيارات الحوار في Word.
type: docs
weight: 50
url: /ar/net/aspose.words/document/compatibilityoptions/
---
## Document.CompatibilityOptions property

يوفر الوصول إلى خيارات توافق المستندات (أي تفضيلات المستخدم التي تم إدخالها في ملف **التوافق** علامة التبويب **خيارات** الحوار في Word).

```csharp
public CompatibilityOptions CompatibilityOptions { get; }
```

### أمثلة

يوضح كيفية تحسين المستند لإصدارات مختلفة من Microsoft Word.

```csharp
public void OptimizeFor()
{
    Document doc = new Document();

    // يحتوي هذا الكائن على قائمة واسعة من العلامات الفريدة لكل مستند
    // التي تتيح لنا تسهيل التوافق مع الإصدارات القديمة من Microsoft Word.
    CompatibilityOptions options = doc.CompatibilityOptions;

    // اطبع الإعدادات الافتراضية لمستند فارغ.
    Console.WriteLine("\nDefault optimization settings:");
    PrintCompatibilityOptions(options);

    // يمكننا الوصول إلى هذه الإعدادات في Microsoft Word عبر "ملف" -> "الخيارات" -> "متقدم" -> "خيارات التوافق لـ...".
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
/// يجمع كل العلامات الموجودة في كائن خيارات توافق المستند حسب الحالة، ثم يطبع كل مجموعة.
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

* class [CompatibilityOptions](../../../aspose.words.settings/compatibilityoptions/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)


