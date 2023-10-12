---
title: FontSourceBase.WarningCallback
second_title: Aspose.Words لمراجع .NET API
description: FontSourceBase ملكية. يتم استدعاؤه أثناء معالجة مصدر الخط عند اكتشاف مشكلة قد تؤدي إلى فقدان دقة التنسيق.
type: docs
weight: 30
url: /ar/net/aspose.words.fonts/fontsourcebase/warningcallback/
---
## FontSourceBase.WarningCallback property

يتم استدعاؤه أثناء معالجة مصدر الخط عند اكتشاف مشكلة قد تؤدي إلى فقدان دقة التنسيق.

```csharp
public IWarningCallback WarningCallback { get; set; }
```

### أمثلة

يوضح كيفية استدعاء رد الاتصال التحذيري عند التعامل مع مصادر الخطوط.

```csharp
public void FontSourceWarning()
{
    FontSettings settings = new FontSettings();
    settings.SetFontsFolder("bad folder?", false);

    FontSourceBase source = settings.GetFontsSources()[0];
    FontSourceWarningCollector callback = new FontSourceWarningCollector();
    source.WarningCallback = callback;

    // احصل على قائمة الخطوط للاتصال بتحذير رد الاتصال.
    IList<PhysicalFontInfo> fontInfos = source.GetAvailableFonts();

    Assert.True(callback.FontSubstitutionWarnings[0].Description
        .Contains("Error loading font from the folder \"bad folder?\""));
}

private class FontSourceWarningCollector : IWarningCallback
{
    /// <summary>
    /// يتم الاتصال به في كل مرة يحدث فيها تحذير أثناء معالجة مصدر الخط.
    /// </summary>
    public void Warning(WarningInfo info)
    {
        FontSubstitutionWarnings.Warning(info);
    }

    public readonly WarningInfoCollection FontSubstitutionWarnings = new WarningInfoCollection();
}
```

### أنظر أيضا

* interface [IWarningCallback](../../../aspose.words/iwarningcallback/)
* class [FontSourceBase](../)
* مساحة الاسم [Aspose.Words.Fonts](../../fontsourcebase/)
* المجسم [Aspose.Words](../../../)


