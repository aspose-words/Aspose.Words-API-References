---
title: StreamFontSource Class
linktitle: StreamFontSource
articleTitle: StreamFontSource
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Fonts.StreamFontSource، الحل الأمثل للحصول على مصادر خطوط مخصصة تعمل على تحسين مرونة المستندات وتصميمها.
type: docs
weight: 3470
url: /ar/net/aspose.words.fonts/streamfontsource/
---
## StreamFontSource class

الفئة الأساسية لمصدر الخط المباشر المحدد من قبل المستخدم.

لمعرفة المزيد، قم بزيارة[العمل مع الخطوط](https://docs.aspose.com/words/net/working-with-fonts/) مقالة توثيقية.

```csharp
public abstract class StreamFontSource : FontSourceBase,   
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [CacheKey](../../aspose.words.fonts/streamfontsource/cachekey/) { get; } | مفتاح هذا المصدر في ذاكرة التخزين المؤقت. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | يعيد أولوية مصدر الخط. |
| [Type](../../aspose.words.fonts/streamfontsource/type/) { get; } | يعيد نوع مصدر الخط. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | يتم استدعاؤها أثناء معالجة مصدر الخط عند اكتشاف مشكلة قد تؤدي إلى فقدان دقة التنسيق. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | إرجاع قائمة الخطوط المتوفرة عبر هذا المصدر. |
| abstract [OpenFontDataStream](../../aspose.words.fonts/streamfontsource/openfontdatastream/)() | يجب أن تفتح هذه الطريقة التدفق ببيانات الخط عند الطلب. |

## ملاحظات

لكي تتمكن من استخدام مصدر الخط المتدفق، يجب عليك إنشاء فئة مشتقة من`StreamFontSource` وتوفير التنفيذ لـ[`OpenFontDataStream`](./openfontdatastream/) طريقة.

[`OpenFontDataStream`](./openfontdatastream/)يمكن استدعاء هذه الطريقة عدة مرات. في المرة الأولى، سيتم استدعاؤها بـ عندما يفحص Aspose.Words مصادر الخطوط المُقدمة للحصول على قائمة الخطوط المتاحة. لاحقًا، قد يتم استدعاؤها إذا استُخدم الخط في المستند لتحليل بيانات الخط وتضمينها في بعض تنسيقات الإخراج.

`StreamFontSource` قد يكون مفيدًا لأنه يسمح بتحميل بيانات الخط فقط عندما تكون مطلوبة وليس تخزينها في الذاكرة لـ[`FontSettings`](../fontsettings/) حياة.

## أمثلة

يوضح كيفية تحميل الخطوط من الدفق.

```csharp
public void StreamFontSourceFileRendering()
{
    FontSettings fontSettings = new FontSettings();
    fontSettings.SetFontsSources(new FontSourceBase[] {new StreamFontSourceFile()});

    DocumentBuilder builder = new DocumentBuilder();
    builder.Document.FontSettings = fontSettings;
    builder.Font.Name = "Kreon-Regular";
    builder.Writeln("Test aspose text when saving to PDF.");

    builder.Document.Save(ArtifactsDir + "FontSettings.StreamFontSourceFileRendering.pdf");
}

/// <summary>
/// قم بتحميل بيانات الخط فقط عند الحاجة إليها بدلاً من تخزينها في الذاكرة
/// طوال عمر كائن "FontSettings".
/// </summary>
private class StreamFontSourceFile : StreamFontSource
{
    public override Stream OpenFontDataStream()
    {
        return File.OpenRead(FontsDir + "Kreon-Regular.ttf");
    }
}
```

### أنظر أيضا

* class [FontSourceBase](../fontsourcebase/)
* interface [  ](../../global/%02  /)
* مساحة الاسم [Aspose.Words.Fonts](../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../)
