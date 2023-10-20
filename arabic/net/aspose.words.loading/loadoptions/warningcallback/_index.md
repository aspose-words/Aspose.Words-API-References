---
title: LoadOptions.WarningCallback
linktitle: WarningCallback
articleTitle: WarningCallback
second_title: Aspose.Words لـ .NET
description: LoadOptions WarningCallback ملكية. يتم استدعاؤه أثناء عملية التحميل عند اكتشاف مشكلة قد تؤدي إلى فقدان دقة البيانات أو التنسيق في C#.
type: docs
weight: 170
url: /ar/net/aspose.words.loading/loadoptions/warningcallback/
---
## LoadOptions.WarningCallback property

يتم استدعاؤه أثناء عملية التحميل، عند اكتشاف مشكلة قد تؤدي إلى فقدان دقة البيانات أو التنسيق.

```csharp
public IWarningCallback WarningCallback { get; set; }
```

## أمثلة

يوضح كيفية طباعة وتخزين التحذيرات التي تحدث أثناء تحميل المستندات.

```csharp
public void LoadOptionsWarningCallback()
{
    // قم بإنشاء كائن LoadOptions جديد وقم بتعيين سمة وارنكالباك الخاصة به
    // كمثال لتطبيق IWarningCallback الخاص بنا.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.WarningCallback = new DocumentLoadingWarningCallback();

    // سوف يقوم رد الاتصال الخاص بنا بطباعة جميع التحذيرات التي تظهر أثناء عملية التحميل.
    Document doc = new Document(MyDir + "Document.docx", loadOptions);

    List<WarningInfo> warnings = ((DocumentLoadingWarningCallback)loadOptions.WarningCallback).GetWarnings();
    Assert.AreEqual(3, warnings.Count);
}

/// <summary>
/// IWarningCallback الذي يطبع التحذيرات وتفاصيلها عند ظهورها أثناء تحميل المستند.
/// </summary>
private class DocumentLoadingWarningCallback : IWarningCallback
{
    public void Warning(WarningInfo info)
    {
        Console.WriteLine($"Warning: {info.WarningType}");
        Console.WriteLine($"\tSource: {info.Source}");
        Console.WriteLine($"\tDescription: {info.Description}");
        mWarnings.Add(info);
    }

    public List<WarningInfo> GetWarnings()
    {
        return mWarnings;
    }

    private readonly List<WarningInfo> mWarnings = new List<WarningInfo>();
}
```

### أنظر أيضا

* interface [IWarningCallback](../../../aspose.words/iwarningcallback/)
* class [LoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)
