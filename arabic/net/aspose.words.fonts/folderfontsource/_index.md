---
title: FolderFontSource Class
linktitle: FolderFontSource
articleTitle: FolderFontSource
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Fonts.FolderFontSource، الحل الأمثل لإدارة خطوط TrueType بكفاءة. حسّن جودة طباعة مستندك اليوم!
type: docs
weight: 3290
url: /ar/net/aspose.words.fonts/folderfontsource/
---
## FolderFontSource class

يمثل المجلد الذي يحتوي على ملفات خطوط TrueType.

لمعرفة المزيد، قم بزيارة[العمل مع الخطوط](https://docs.aspose.com/words/net/working-with-fonts/) مقالة توثيقية.

```csharp
public class FolderFontSource : FontSourceBase
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [FolderFontSource](folderfontsource/#constructor)(*string, bool*) | المولد. |
| [FolderFontSource](folderfontsource/#constructor_1)(*string, bool, int*) | المولد. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [FolderPath](../../aspose.words.fonts/folderfontsource/folderpath/) { get; } | المسار إلى المجلد. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | يعيد أولوية مصدر الخط. |
| [ScanSubfolders](../../aspose.words.fonts/folderfontsource/scansubfolders/) { get; } | يحدد ما إذا كان سيتم مسح المجلدات الفرعية أم لا. |
| override [Type](../../aspose.words.fonts/folderfontsource/type/) { get; } | يعيد نوع مصدر الخط. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | يتم استدعاؤها أثناء معالجة مصدر الخط عند اكتشاف مشكلة قد تؤدي إلى فقدان دقة التنسيق. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | إرجاع قائمة الخطوط المتوفرة عبر هذا المصدر. |

## أمثلة

يوضح كيفية استخدام مجلد النظام المحلي الذي يحتوي على الخطوط كمصدر للخطوط.

```csharp
// قم بإنشاء مصدر الخط من مجلد يحتوي على ملفات الخطوط.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false, 1);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

Assert.AreEqual(FontsDir, folderFontSource.FolderPath);
Assert.AreEqual(false, folderFontSource.ScanSubfolders);
Assert.AreEqual(FontSourceType.FontsFolder, folderFontSource.Type);
Assert.AreEqual(1, folderFontSource.Priority);
```

### أنظر أيضا

* class [FontSourceBase](../fontsourcebase/)
* مساحة الاسم [Aspose.Words.Fonts](../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../)
