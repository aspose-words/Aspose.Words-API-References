---
title: FontSourceBase Class
linktitle: FontSourceBase
articleTitle: FontSourceBase
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.Fonts.FontSourceBase، الفئة المجردة الأساسية لتحديد مصادر الخطوط المتنوعة في تطبيقاتك. حسّن تنسيق مستنداتك!
type: docs
weight: 3410
url: /ar/net/aspose.words.fonts/fontsourcebase/
---
## FontSourceBase class

هذه فئة أساسية مجردة للفئات التي تسمح للمستخدم بتحديد مصادر الخطوط المختلفة.

لمعرفة المزيد، قم بزيارة[العمل مع الخطوط](https://docs.aspose.com/words/net/working-with-fonts/) مقالة توثيقية.

```csharp
public abstract class FontSourceBase
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | يعيد أولوية مصدر الخط. |
| abstract [Type](../../aspose.words.fonts/fontsourcebase/type/) { get; } | يعيد نوع مصدر الخط. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | يتم استدعاؤها أثناء معالجة مصدر الخط عند اكتشاف مشكلة قد تؤدي إلى فقدان دقة التنسيق. |

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

* مساحة الاسم [Aspose.Words.Fonts](../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../)
