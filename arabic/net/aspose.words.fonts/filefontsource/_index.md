---
title: FileFontSource Class
linktitle: FileFontSource
articleTitle: FileFontSource
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Fonts.FileFontSource فصل. يمثل ملف خط TrueType الفردي المخزن في نظام الملفات في C#.
type: docs
weight: 2870
url: /ar/net/aspose.words.fonts/filefontsource/
---
## FileFontSource class

يمثل ملف خط TrueType الفردي المخزن في نظام الملفات.

لمعرفة المزيد، قم بزيارة[العمل مع الخطوط](https://docs.aspose.com/words/net/working-with-fonts/) مقالة توثيقية.

```csharp
public class FileFontSource : FontSourceBase
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FileFontSource](filefontsource/#constructor)(*string*) | الممثل. |
| [FileFontSource](filefontsource/#constructor_1)(*string, int*) | الممثل. |
| [FileFontSource](filefontsource/#constructor_2)(*string, int, string*) | الممثل. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [CacheKey](../../aspose.words.fonts/filefontsource/cachekey/) { get; } | مفتاح هذا المصدر في ذاكرة التخزين المؤقت. |
| [FilePath](../../aspose.words.fonts/filefontsource/filepath/) { get; } | المسار إلى ملف الخط. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | يُرجع أولوية مصدر الخط. |
| override [Type](../../aspose.words.fonts/filefontsource/type/) { get; } | إرجاع نوع مصدر الخط. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | يتم استدعاؤه أثناء معالجة مصدر الخط عند اكتشاف مشكلة قد تؤدي إلى فقدان دقة التنسيق. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | إرجاع قائمة الخطوط المتوفرة عبر هذا المصدر. |

## أمثلة

يوضح كيفية استخدام ملف الخط في نظام الملفات المحلي كمصدر للخط.

```csharp
FileFontSource fileFontSource = new FileFontSource(MyDir + "Alte DIN 1451 Mittelschrift.ttf", 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {fileFontSource});

Assert.AreEqual(MyDir + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.FilePath);
Assert.AreEqual(FontSourceType.FontFile, fileFontSource.Type);
Assert.AreEqual(0, fileFontSource.Priority);
```

### أنظر أيضا

* class [FontSourceBase](../fontsourcebase/)
* مساحة الاسم [Aspose.Words.Fonts](../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../)
