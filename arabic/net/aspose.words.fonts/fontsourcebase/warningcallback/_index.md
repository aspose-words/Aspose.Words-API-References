---
title: FontSourceBase.WarningCallback
linktitle: WarningCallback
articleTitle: WarningCallback
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FontSourceBase WarningCallback، وهي ضرورية لضمان دقة التنسيق من خلال اكتشاف المشكلات أثناء معالجة مصدر الخط.
type: docs
weight: 30
url: /ar/net/aspose.words.fonts/fontsourcebase/warningcallback/
---
## FontSourceBase.WarningCallback property

يتم استدعاؤها أثناء معالجة مصدر الخط عند اكتشاف مشكلة قد تؤدي إلى فقدان دقة التنسيق.

```csharp
public IWarningCallback WarningCallback { get; set; }
```

## أمثلة

يوضح كيفية استدعاء معاودة الاتصال التحذيرية عند العمل مع مصادر الخطوط.

```csharp
public void FontSourceWarning()
{
    FontSettings settings = new FontSettings();
    settings.SetFontsFolder("bad folder?", false);

    FontSourceBase source = settings.GetFontsSources()[0];
    FontSourceWarningCollector callback = new FontSourceWarningCollector();
    source.WarningCallback = callback;

    // احصل على قائمة الخطوط التي سيتم استدعاء معاودة الاتصال التحذيرية.
    IList<PhysicalFontInfo> fontInfos = source.GetAvailableFonts();

    Assert.True(callback.FontSubstitutionWarnings[0].Description
        .Contains("Error loading font from the folder \"bad folder?\""));
}

private class FontSourceWarningCollector : IWarningCallback
{
    /// <summary>
    /// يتم استدعاؤها في كل مرة يحدث فيها تحذير أثناء معالجة مصدر الخط.
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
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)
