---
title: StreamFontSource Class
linktitle: StreamFontSource
articleTitle: StreamFontSource
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Fonts.StreamFontSource فصل. الفئة الأساسية لمصدر خط الدفق المحدد من قبل المستخدم في C#.
type: docs
weight: 3040
url: /ar/net/aspose.words.fonts/streamfontsource/
---
## StreamFontSource class

الفئة الأساسية لمصدر خط الدفق المحدد من قبل المستخدم.

لمعرفة المزيد، قم بزيارة[العمل مع الخطوط](https://docs.aspose.com/words/net/working-with-fonts/) مقالة توثيقية.

```csharp
public abstract class StreamFontSource : FontSourceBase
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [CacheKey](../../aspose.words.fonts/streamfontsource/cachekey/) { get; } | مفتاح هذا المصدر في ذاكرة التخزين المؤقت. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | يُرجع أولوية مصدر الخط. |
| [Type](../../aspose.words.fonts/streamfontsource/type/) { get; } | إرجاع نوع مصدر الخط. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | يتم استدعاؤه أثناء معالجة مصدر الخط عند اكتشاف مشكلة قد تؤدي إلى فقدان دقة التنسيق. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | إرجاع قائمة الخطوط المتوفرة عبر هذا المصدر. |
| abstract [OpenFontDataStream](../../aspose.words.fonts/streamfontsource/openfontdatastream/)() | يجب أن تفتح هذه الطريقة الدفق ببيانات الخط حسب الطلب. |

## ملاحظات

من أجل استخدام مصدر خط الدفق، يجب عليك إنشاء فئة مشتقة من`StreamFontSource` وتوفير تنفيذ[`OpenFontDataStream`](./openfontdatastream/) طريقة.

[`OpenFontDataStream`](./openfontdatastream/)يمكن استدعاء الطريقة عدة مرات. لأول مرة سيتم استدعاؤه عندما يقوم Aspose.Words بمسح مصادر الخطوط المتوفرة للحصول على قائمة الخطوط المتاحة. قد يتم استدعاؤه لاحقًا إذا تم استخدام الخط في المستند لتحليل بيانات الخط وتضمين بيانات الخط في بعض تنسيقات الإخراج.

`StreamFontSource` قد يكون مفيدًا لأنه يسمح بتحميل بيانات الخط فقط عندما تكون مطلوبة وليس تخزينها في الذاكرة[`FontSettings`](../fontsettings/) حياة.

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
* مساحة الاسم [Aspose.Words.Fonts](../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../)
