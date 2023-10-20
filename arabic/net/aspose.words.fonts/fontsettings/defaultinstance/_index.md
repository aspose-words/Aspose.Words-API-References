---
title: FontSettings.DefaultInstance
linktitle: DefaultInstance
articleTitle: DefaultInstance
second_title: Aspose.Words لـ .NET
description: FontSettings DefaultInstance ملكية. إعدادات الخط الافتراضية الثابتة في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.fonts/fontsettings/defaultinstance/
---
## FontSettings.DefaultInstance property

إعدادات الخط الافتراضية الثابتة.

```csharp
public static FontSettings DefaultInstance { get; }
```

## ملاحظات

يتم استخدام هذا المثيل افتراضيًا في المستند ما لم[`FontSettings`](../../../aspose.words/document/fontsettings/) تم تحديده.

## أمثلة

يوضح كيفية تكوين مثيل إعدادات الخط الافتراضي.

```csharp
// قم بتكوين مثيل إعدادات الخط الافتراضي لاستخدام الخط "Courier New".
// كبديل احتياطي عندما نحاول استخدام خط غير معروف.
FontSettings.DefaultInstance.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Courier New";

Assert.True(FontSettings.DefaultInstance.SubstitutionSettings.DefaultFontSubstitution.Enabled);

Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Non-existent font";
builder.Write("Hello world!");

// لا يحتوي هذا المستند على تكوين إعدادات الخط. عندما نقوم بتسليم الوثيقة
// سوف يقوم مثيل FontSettings الافتراضي بحل الخط المفقود.
// Aspose.Words سيستخدم "Courier New" لعرض النص الذي يستخدم الخط غير المعروف.
Assert.Null(doc.FontSettings);

doc.Save(ArtifactsDir + "FontSettings.DefaultFontInstance.pdf");
```

يوضح كيفية استخدام واجهة IWarningCallback لمراقبة تحذيرات استبدال الخط.

```csharp
public void SubstitutionWarning()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Font.Name = "Times New Roman";
    builder.Writeln("Hello world!");

    FontSubstitutionWarningCollector callback = new FontSubstitutionWarningCollector();
    doc.WarningCallback = callback;

    // قم بتخزين المجموعة الحالية من مصادر الخطوط، والتي ستكون مصدر الخط الافتراضي لكل مستند
    // الذي لا نحدد له مصدر خط مختلف.
    FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

    // لأغراض الاختبار، سنقوم بتعيين Aspose.Words للبحث عن الخطوط في مجلد غير موجود فقط.
    FontSettings.DefaultInstance.SetFontsFolder(string.Empty, false);

    // عند عرض المستند، لن يكون هناك مكان للعثور على الخط "Times New Roman".
    // سيؤدي هذا إلى ظهور تحذير بشأن استبدال الخط، والذي سيكتشفه رد الاتصال الخاص بنا.
    doc.Save(ArtifactsDir + "FontSettings.SubstitutionWarning.pdf");

    FontSettings.DefaultInstance.SetFontsSources(originalFontSources);

    Assert.True(callback.FontSubstitutionWarnings[0].WarningType == WarningType.FontSubstitution);
    Assert.True(callback.FontSubstitutionWarnings[0].Description
        .Equals(
            "Font 'Times New Roman' has not been found. Using 'Fanwood' font instead. Reason: first available font.", StringComparison.Ordinal));
}

private class FontSubstitutionWarningCollector : IWarningCallback
{
    /// <summary>
    /// يتم الاتصال به في كل مرة يحدث فيها تحذير أثناء التحميل/الحفظ.
    /// </summary>
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.FontSubstitution)
            FontSubstitutionWarnings.Warning(info);
    }

    public WarningInfoCollection FontSubstitutionWarnings = new WarningInfoCollection();
}
```

### أنظر أيضا

* class [FontSettings](../)
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)
