---
title: MemoryFontSource Class
linktitle: MemoryFontSource
articleTitle: MemoryFontSource
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Fonts.MemoryFontSource، التي تتيح الوصول بشكل سلس إلى خطوط TrueType المخزنة في الذاكرة لتحسين معالجة المستندات.
type: docs
weight: 3450
url: /ar/net/aspose.words.fonts/memoryfontsource/
---
## MemoryFontSource class

يمثل ملف الخط TrueType الوحيد المخزن في الذاكرة.

لمعرفة المزيد، قم بزيارة[العمل مع الخطوط](https://docs.aspose.com/words/net/working-with-fonts/) مقالة توثيقية.

```csharp
public class MemoryFontSource : FontSourceBase
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [MemoryFontSource](memoryfontsource/#constructor)(*byte[]*) | المولد. |
| [MemoryFontSource](memoryfontsource/#constructor_1)(*byte[], int*) | المولد. |
| [MemoryFontSource](memoryfontsource/#constructor_2)(*byte[], int, string*) | المولد. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [CacheKey](../../aspose.words.fonts/memoryfontsource/cachekey/) { get; } | مفتاح هذا المصدر في ذاكرة التخزين المؤقت. |
| [FontData](../../aspose.words.fonts/memoryfontsource/fontdata/) { get; } | بيانات الخط الثنائية. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | يعيد أولوية مصدر الخط. |
| override [Type](../../aspose.words.fonts/memoryfontsource/type/) { get; } | يعيد نوع مصدر الخط. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | يتم استدعاؤها أثناء معالجة مصدر الخط عند اكتشاف مشكلة قد تؤدي إلى فقدان دقة التنسيق. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | إرجاع قائمة الخطوط المتوفرة عبر هذا المصدر. |

## أمثلة

يوضح كيفية استخدام مجموعة بايتات تحتوي على بيانات من ملف الخط كمصدر للخط.

```csharp
byte[] fontBytes = File.ReadAllBytes(MyDir + "Alte DIN 1451 Mittelschrift.ttf");
MemoryFontSource memoryFontSource = new MemoryFontSource(fontBytes, 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {memoryFontSource});

Assert.AreEqual(FontSourceType.MemoryFont, memoryFontSource.Type);
Assert.AreEqual(0, memoryFontSource.Priority);
```

### أنظر أيضا

* class [FontSourceBase](../fontsourcebase/)
* مساحة الاسم [Aspose.Words.Fonts](../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../)
